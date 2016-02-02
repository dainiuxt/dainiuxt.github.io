---
published: true
title: "Install/Update Portable R and RStudio on Windows"
layout: post
---

If you should work on windows machine where you don't have administrative privilegies, you can very easily make portable R/Rstudio installation.

Download [recent version of R](https://cran.r-project.org/) from CRAN site and recent version of [RStudio](https://www.rstudio.com/products/rstudio/download/). After download extract RStudio installation exec with 7Zip and copy files from $_OUTDIR to desired location (in case you making an update, simply overwrite all files, that already exist). Your RStudio executable will be in

~~~
your-chosen-directory/bin/rstudio.exe
~~~

Then run CRAN-R installation, ignore warning that you don't have administrative privilegies and go forward untill installation will complete. Run RStudio, from menu

~~~
Tools->Global Options
~~~

locate where your R installation is located.

If you performing update (more recent version of R), copy all files from *library* subfolder of old R installation into new, but this time DON'T OVERWRITE! This operation vill preserve the packages you have installed in previous version of R. After copying update all your packages from RStudio window (Packages->Update). When packages update process will end check which packages failed to update (You will see warning messages near them in RStudio console). Remove these packages (write down names of failed packages and delete corresponding folders from *library* subfolder). For this you will ned to exit from RStudio. After deletion lauch RStudio again and execute packages install command in RStudio console:

{% highlight r %}
install.packages(c("package1", "package2", "package3"))
{% endhighlight %}

Congratulations, You are ready to go!
