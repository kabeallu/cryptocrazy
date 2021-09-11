---
title: Create a blog free on github using jekyll
date: 2021-07-26
categories: [linux, guides]
tags: []

#image:
#  src: /assets/img/hackthebox/boxes/cap/cap-box.png
#  width: 600   # in pixels
#  height: 300   # in pixels
#  alt: cap
---


### Use ssh keys to manage github without using access tokens or passwords

#### Generate ssh key pair in your terminal
{% highlight bash %}
ssh-keygen -t rsa -b 4096 -C "kabeallu@protonmail.com"
{% endhighlight %}


#### Start ssh-agent in the background
{% highlight bash %}
eval "$(ssh-agent -s)"
{% endhighlight %}

#### add private key to ssh-agent
{% highlight bash %}
ssh-add ~/.ssh/id_rsa.pub
{% endhighlight %}


#### Test ssh connection
{% highlight bash %}
ssh -T git@github.com
{% endhighlight %}



#### sub heading needed
{% highlight bash %}
git remote set-url origin git@github.com:kabeallu/notes.git
{% endhighlight %}

now we can push pull without username or password


Create a directory to store your site files
{% highlight bash %}
mkdir ~/github/notes
{% endhighlight %}

Change into that new directory and initiate git
{% highlight bash %}
cd ~/github/notes && git init
{% endhighlight %}

{% highlight bash %}
git remote add origin https://github.com/kabeallu/notes.git
{% endhighlight %}

Create Jekyll site
{% highlight bash %}
jekyll new .
{% endhighlight %}

  git config --global user.name "Your Name"
  git config --global user.email "you@example.com"


Add all files and directories ready to be pushed to your repo
{% highlight bash %}
git add -A
{% endhighlight %}

Add a commit comment to your push
{% highlight bash %}
git commit -m 'push'
{% endhighlight %}

push the files to your github accout
{% highlight bash %}
git push -u origin main
{% endhighlight %}

If you encounter an error, It may need to be forced to overwrite existing files.
{% highlight bash %}
git push -u origin main --force
{% endhighlight %}

### TO SORT
First, remove all files from your Git repository using: git rm -r *

After that you should commit: using git commit -m "your comment"

After that you push using: git push (that's update the origin repository)

To verify your status using: git status

After that you can copy all your local files in the local Git folder, and you add them to the Git repository using: git add -A

You commit (git commit -m "your comment" and you push (git push)
