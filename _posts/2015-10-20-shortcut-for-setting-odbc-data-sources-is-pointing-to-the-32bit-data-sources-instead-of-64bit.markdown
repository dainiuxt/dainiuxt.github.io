---
published: true
title: Shortcut for setting ODBC data sources is pointing to the 32bit data sources instead of 64bit
layout: post
---
Go to control panel -> administrative tools --> select data sources(ODBC) --> then right click on that file --> go to properties --> in the shortcut tab -> change the path from %windir%\System32\odbcad32.exe to

{% highlight ruby %}
%windir%\SysWOW64\odbcad32.exe
{% endhighlight %} 