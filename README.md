# RPi-Scripts
Utility scripts for Raspberry Pi projects, such as network watchdog, autostart apps, etc.

##PM2
Make sure that the shell scripts are executable (chmod +x <scriptname>.sh)

Install: sudo npm install -g pm2
Run PM2 on startup: pm2 startup
Register shell script with PM2: pm2 start mm.sh
Save PM2 scripts across reboots: pm2 save

Usefull PM2 commands:
pm2 restart <script>
pm2 stop <script>
pm2 logs <script>
pm2 show <script>
