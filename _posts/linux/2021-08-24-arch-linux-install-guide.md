---
title: Arch Linux Install Guide
date: 2021-08-24
categories: [linux, guides]
tags: []

#image:
#  src: /assets/img/hackthebox/boxes/cap/cap-box.png
#  width: 600   # in pixels
#  height: 300   # in pixels
#  alt: cap
---
#### Update system clock
{% highlight bash %}
timedatectl set-ntp true
{% endhighlight %}

#### Partition the drive
{% highlight bash %}
fdisk /dev/sda
{% endhighlight %}

#### Format the partitions
{% highlight bash %}
mkfs.ext4 /dev/sda2
{% endhighlight %}

#### Format the partitions
{% highlight bash %}
mkswap /dev/sda1
{% endhighlight %}

#### Mount the file systems
{% highlight bash %}
mount /dev/sda2 /mnt
{% endhighlight %}

#### Turn Swap partition on
{% highlight bash %}
swapon /dev/sda1
{% endhighlight %}

#### Install essential packages
{% highlight bash %}
pacstrap /mnt base linux linux-firmware nano
{% endhighlight %}

### Configure the system

#### Fstab
{% highlight bash %}
 genfstab -U /mnt >> /mnt/etc/fstab
 {% endhighlight %}

####  Chroot
{% highlight bash %}
arch-chroot /mnt
{% endhighlight %}

#### Time zone
Set the time zone
{% highlight bash %}
ln -sf /usr/share/zoneinfo/Region/City /etc/localtime
{% endhighlight %}

{% highlight bash %}
hwclock --systohc
{% endhighlight %}

# more to follow
