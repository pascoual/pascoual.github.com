---
layout: post
title: "Measuring JavaScript execution times [US]"
modified: 2014-05-20 10:45:56 +0200
tags: [JavaScript, time]
image:
  feature: abstract-4.jpg
  credit:
  creditlink:
comments: true
share: true
---

Want to see if you implementation is time consuming ?


## console.time()

You can use console.time like this:

{% highlight javascript %}
var counter = "";

// Start timing now with a TAG (allow you to do more than one verification at a time)
console.time("myOppTag");

for (var i = 1; i <= 1e3; i++)
    counter += i;

// ... and stop with the same TAG (No? You kidding ?)
console.timeEnd("myOppTag");

// Just for fun
console.log("Outch: " + counter);
{% endhighlight %}

You will get this in the console:
{% highlight javascript %}
myOppTag: 19.913ms
{% endhighlight %}


## I need to put the result in a variable!

Ok, you need to log it in you DB or to do anything else with it? You just need to do it the old way!
{% highlight javascript %}
var counter = "";
var myTimer = {};
// Remember when we started
myTimer.start = new Date().getTime();

for (var i = 1; i <= 1e3; i++)
    counter += i;

// Remember when we finished
myTimer.end = new Date().getTime();

// Now calculate and output the difference
myTimer.result = myTimer.end - myTimer.start;
console.log(myTimer.result +' ms');

// Just for fun
console.log("Outch: " + counter);
{% endhighlight %}


## Warning: timekeeper note

The accuracy and precision depend of your browser and your OS.
<img src="/images/posts/accuracy_precision.png" alt="" class="img-rounded">


## Precision with BenchmarkJS as opt/sec

But if you want precision just use [BenchmarkJS](http://benchmarkjs.com/), it will give you results as ops/sec (higher is better).

[<img src="/images/posts/benchmarkjs1.jpg" alt="" class="img-rounded">](http://jsperf.com/if-vs-switch-vadim)
[jsperf](http://jsperf.co) use [BenchmarkJS](http://benchmarkjs.com/)
