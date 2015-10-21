---
published: true
title: Connect MS Access database (.accdb) to R under Win7(x64)
layout: post
---
The very first tip for this case is you should use 32 bit version of R. To change your active R version you can go in menu Tools->Global Options while using Rstudio IDE and select prefered version of R.

{% highlight r %}
library("RODBC") #load package
db<-file.path("C:/path/to/your/database.accdb") #connect database.
#Note the UNIX style slash (/). "\" is "escape character" so all "\"  you should replace either with "/" or "\\"
channel<-odbcConnectAccess2007(db) #internal RODBC function
dataSetName<-sqlFetch(channel,"TableName") #read particular table from Access database file.
close(channel) #do not forget this, otherwise you lock access database from editing.
{% endhighlight %} 

So far this works only in Windows but not in linux.