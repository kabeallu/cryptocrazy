---
title: Proxychains And Tor On Kali
date: 2021-09-15
categories: [linux, kali]
tags: []

#image:
#  src: /assets/img/hackthebox/boxes/cap/cap-box.png
#  width: 600   # in pixels
#  height: 300   # in pixels
#  alt: cap
---


## Tor On Kali
Description
### Installing Tor
Installing is easy on kali
```
sudo apt install tor
```
### Using Tor
Starting the service
```
sudo service tor start
```
Stoping the service
```
sudo service tor Stop
```
Checking the status
```
sudo service tor status
```

## Proxychains On kali
Description
### Installing Proxychains
```
sudo apt install proxychains
```
### Configuring Proxychains
Edit the proxychains config file
```
sudo nano /etc/proxychains.conf
```

Dynamic

Strict

Random

Comment out the socks4  127.0.0.1 9050 line to disable tor network
```
[ProxyList]
# add proxy here ...
# meanwile
# defaults set to "tor"
#socks4         127.0.0.1 9050
```
