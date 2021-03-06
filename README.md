# RPi-Scripts
Utility scripts for Raspberry Pi projects, such as network watchdog, autostart apps, etc.

## PM2
Make sure that the shell scripts are executable (`chmod +x myscript.sh` or `chmod 775 myscript.sh`)

Install `sudo npm install -g pm2`

Run PM2 on startup `pm2 startup`

Register shell script with PM2 `pm2 start myscript.sh`
  
Save PM2 scripts across reboots `pm2 save`

Usefull PM2 commands:
* `pm2 restart myscript`
* `pm2 stop myscript`
* `pm2 logs myscript`
* `pm2 show myscript`

## crontab
Open crontab editor `crontab -e`

Run the scripts every 5 minutes writing the output to /dev/null so it won't clog the syslog

`*/5 * * * * /usr/bin/sudo -H /usr/local/bin/myscript.sh >> /dev/null 2>&1`
