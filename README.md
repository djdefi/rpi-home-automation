# rpi-home-automation

Docker based home automation server running on a Raspberry Pi.

## Hardware
* [Raspberry Pi 2 (Starter Kit from Canakit.com)](https://www.canakit.com/raspberry-pi-starter-kit.html)
* [Bloomsky](https://www.bloomsky.com/#product) - Weather station
* [FireTV Stick](https://smile.amazon.com/Amazon-Fire-TV-Stick-Streaming-Media-Player/dp/B00GDQ0RMG/) - Media

## Base OS
* [Hypriot OS](http://blog.hypriot.com/downloads/) - Docker RPi image ready to rock and roll

## Custom RPi Containers

Conversions to ARM and other tweaks.

* [RPi alpine scratch](https://github.com/djdefi/rpi-alpine-scratch) - Used as a base image
* [nginx](https://github.com/djdefi/rpi-nginx) - Used as a base image
* [DuckDNS](https://github.com/djdefi/docker-duckdns) - Dynamic DNS
* [Home Assistant](https://github.com/djdefi/docker-rpi-home-assistant) - https://home-assistant.io
* [nginx proxy](https://github.com/djdefi/rpi-nginx-proxy) - Reverse proxy for services
* [Let's Encrypt nginx proxy helper](https://github.com/djdefi/docker-letsencrypt-nginx-proxy-companion) - [Let's Encrypt](https://letsencrypt.org/) Automatic SSL Certs
* [firetv-server](https://github.com/djdefi/rpi-firetvserver) - Control Amazon FireTV
* [ProFTPD](https://github.com/djdefi/rpi-docker-proftpd) - FTP target for Foscam capture
* [Jenkins](https://github.com/djdefi/rpi-jenkins) - Automate Docker image builds
