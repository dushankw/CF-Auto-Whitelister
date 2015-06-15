CloudFlare Automatic Whitelister
===================

## The problem
* You have a web server and you only want it to be accessible via CloudFlare.
* Somehow though, people keep finding the servers real IP address (since 80 and 443 are open to the world) and are doing bad things.
* You could restrict 80 and 443 so only CloudFlare subnets can connect, but what if CloudFlare add/change IP addresses?

## The answer
* This script will get all the current CloudFlare IP addresses and allow them on ports 80 and 443.
* Just add it to the root users crontab and run as often as you like (I personally do it weekly).

## Requirements
* A Debian/Ubuntu server with UFW installed and enabled as the system Firewall.

## Assumptions
* Written for IPv4 addressing only.

## Missing Features
* Script does not account for any IP addresses CloudFlare have removed, I don't think this is a massive issue but I will fix it eventually (or you could send me a pull request).
