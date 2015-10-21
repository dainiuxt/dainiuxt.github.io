---
published: true
title: Install R packages on demand (if require) 
layout: post
---
{% highlight ruby %}
if (!require("data.table")) {
install.packages("data.table")
}
if (!require("reshape2")) {
install.packages("reshape2")
}
require("data.table")
require("reshape2")
{% endhighlight %} 