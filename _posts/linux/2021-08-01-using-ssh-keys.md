---
title: Create SSH keys and use them on your linux systems
date: 2021-08-01
categories: [linux, guides]
tags: []

#image:
#  src: /assets/img/hackthebox/boxes/cap/cap-box.png
#  width: 600   # in pixels
#  height: 300   # in pixels
#  alt: cap
---
Generate your ssh key pair
{% highlight bash %}
ssh-keygen
{% endhighlight %}

{% highlight bash %}
nano ~/.ssh/config  
{% endhighlight %}

{% highlight bash %}
Host github.com
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_rsa
  IdentitiesOnly yes
{% endhighlight %}
