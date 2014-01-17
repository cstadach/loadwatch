#LoadWatch 

## Email notification + diagnostics emailed when a preset server load is triggerd.  


### Install

To install loadwatch.sh manually: 


```mkdir /root/bin
mkdir /root/loadwatch
touch /root/bin/loadwatch.sh
chmod 700 /root/bin/loadwatch.sh
vim /root/bin/loadwatch.sh    #(copy and paste loadwatch.sh into here)
```

Next, edit your crontab and insert the entry below which will run loadwatch.sh every 3 minutes to check server load and generate a report of the load is over the set threshold.

```
crontab -e     #edit yor

*/3 * * * * /root/bin/loadwatch.sh > /dev/null 2>&1
```


### Configure

Edit loadwatch.sh and set the load level and notification email address you want to use. 

For a single CPU server using '4' for the load level is fairly typical. 


