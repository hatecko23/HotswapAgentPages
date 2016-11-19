---
layout: page
title: "Eclipse setup"
category: ide
date: 2016-11-20 12:44:58
order: 2
---
**Step-1:** Install ?jvm.dll? DCEVM patch in JDK

Follow the same steps which are mentioned on [HotswapAgent quick start page - Install section](http://hotswapagent.org/quick-start) to patch Java Hotspot(r) file in JDK 1.7_xy and download HotswapAgent.jar file.

**Step-2:** In Eclipse - Tomcat Server - Runtime Environment - JRE must be mapped to the same JRE of JDK in which DECVM is patched in step-1

![](https://raw.githubusercontent.com/skybber/HotswapAgentWiki/master/img/EclipseSetup-01.png)

**Step-3:** Tomcat - Add "-XXaltjvm=dcevm -javaagent:<PATH>\HotswapAgent.jar" in VM Arguments.

![](https://raw.githubusercontent.com/skybber/HotswapAgentWiki/master/img/EclipseSetup-02.png)

**Step-4:** Disable ?Auto Reload? in Tomcat web modules
This is most important step, otherwise you will not see power of Hotswap Agent in step-5.

![](https://raw.githubusercontent.com/skybber/HotswapAgentWiki/master/img/EclipseSetup-03.png)

**Step-5:** Run Tomcat in Debug mode and Enjoy java coding.
When you start your server in debug mode, you should see messages like below in Eclipse Console.

![](https://raw.githubusercontent.com/skybber/HotswapAgentWiki/master/img/EclipseSetup-04.png)

Now if you do code changes in java as well as configuration files of supported plugins (i.e. logback.xml), those would be ready for unit testing immediately without server restart.

![](https://raw.githubusercontent.com/skybber/HotswapAgentWiki/master/img/EclipseSetup-05.png)
