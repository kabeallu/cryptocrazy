---
title: Install Telegram On Kali Linux
date: 2021-09-14
categories: [linux, kali]
tags: []

#image:
#  src: /assets/img/hackthebox/boxes/cap/cap-box.png
#  width: 600   # in pixels
#  height: 300   # in pixels
#  alt: cap
---
Install Telegram the Old School Way
Head over to the official Telegram website and download the tar archive. Once it’s done, open up a terminal and navigate to the download directory. Then extract the tar archive.

tar xvf tsetup*.tar.xz
There’ll be a new directory named Telegram and there are two executable files in it: Telegram and Updater.  You can navigate to the Telegram, execute the Telegram file and using Telegram Messenger right away.

cd Telegram

./Telegram
Instead of using Telegram this way, we can move the executable files into /opt.

sudo mv Telegram/ /opt/
Then create a symbolic link

sudo ln -sf /opt/Telegram/Telegram /usr/bin/telegram
File and directory names in Linux are case sensitive.

Now you can launch Telegram by typing telegram in the terminal.
