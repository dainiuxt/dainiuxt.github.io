---
published: true
title: Locale setting in R/RStudio
layout: post
---
If you have different locale from English (usually living outside US or UK), then pretty common problem can be simple task - get weekdays in English from dates.

```
Sys.setlocale("LC_TIME", "C")
```

do the trick and bypass

```
OS reports request to set locale to "EN" cannot be honored
```

error which is pretty common if you use command

```
Sys.setlocale("LC_TIME", "English")
```