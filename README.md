CloudFlare Automatic Whitelister
===================

Assumptions
* A Debian/Ubuntu server with UFW installed and enabled as the system Firewall
* Written for IPv4 addressing only

The problem
* You have a web server, but you only want it to be accessible via CloudFlare
* You could create static Firewall entries for CloudFlare subnets, but they change IP addresses from time to time

The answer
* This script will get all the current CloudFlare IP addresses and allow them on ports 80 and 443
* Just add it to the root users crontab and run as often as you like

Missing Features
* Script does not account for any IP addresses CloudFlare have removed, I don't think this is a massive issue but I will fix it eventually
