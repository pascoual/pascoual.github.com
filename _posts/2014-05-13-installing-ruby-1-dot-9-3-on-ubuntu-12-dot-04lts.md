---
layout: post
title: "Installing Ruby 1.9.3 on Ubuntu 12.04LTS"
modified: 2014-05-13 01:19:52 +0200
tags: [Ubuntu, Linux, Ruby, kramdown, jekyll]
image:
  feature:
  credit:
  creditlink:
comments: true
share: true
---

You can find the US version of this post in [leonard.io](https://leonard.io/blog/2012/05/installing-ruby-1-9-3-on-ubuntu-12-04-precise-pengolin/), a developer in Berlin.

## Vous avez besoin de Ruby 1.9.3 sous Ubuntu 12.04 ?

Pour de multiples raisons, commme l'utilisation de la dernière version de Jekill, vous avez besoin de la version 1.9.3 de Ruby ? Alors vous devez installer la version 1.9.1... Hum ?!? Cherche pas t'as tort !

Dans un terminal:
{% highlight shell-session %}
sudo apt-get update

sudo apt-get install ruby1.9.1 ruby1.9.1-dev \
  rubygems1.9.1 irb1.9.1 ri1.9.1 rdoc1.9.1 \
  build-essential libopenssl-ruby1.9.1 libssl-dev zlib1g-dev

sudo update-alternatives --install /usr/bin/ruby ruby /usr/bin/ruby1.9.1 400 \
         --slave   /usr/share/man/man1/ruby.1.gz ruby.1.gz \
                        /usr/share/man/man1/ruby1.9.1.1.gz \
        --slave   /usr/bin/ri ri /usr/bin/ri1.9.1 \
        --slave   /usr/bin/irb irb /usr/bin/irb1.9.1 \
        --slave   /usr/bin/rdoc rdoc /usr/bin/rdoc1.9.1

# choose your interpreter
# changes symlinks for /usr/bin/ruby , /usr/bin/gem
# /usr/bin/irb, /usr/bin/ri and man (1) ruby
sudo update-alternatives --config ruby
sudo update-alternatives --config gem

# now try
ruby --version
{% endhighlight %}

## Et alors ?

Et bien mon ami, tu as ce que tu voulais, non ? Ok ok j'avoue, il existe bien un packet ruby1.9.3, mais c'est un proxy vers ruby1.9.1.
