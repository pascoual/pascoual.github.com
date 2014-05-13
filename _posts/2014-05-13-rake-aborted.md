---
layout: post
title: "rake aborted!"
modified: 2014-05-13 01:54:35 +0200
tags: [linux, Ubuntu, Ruby, rake, bundle]
image:
  feature:
  credit:
  creditlink:
comments: true
share: true
---

If you get this message trying to run a rake command:
{% highlight shell-session %}
rake aborted!
no such file to load -- bundler/setup
{% endhighlight %}

Run:
{% highlight shell-session %}
gem install bundler
bundle install
bundle exec rake db:create
{% endhighlight %}

You might want to learn about [Bundler](http://gembundler.com/).  
Thanks to [lemoncider](http://stackoverflow.com/users/952064/lemoncider)
