---
layout: page
title: "Netbeans setup"
category: ide
date: 2016-11-20 12:45:13
order: 3
---
**Compile on save:**
![](https://github.com/skybber/HotswapAgentWiki/blob/master/img/NetbeansSetup-01.png)

**Enable automatic Hotswap after compile:**
![](https://github.com/skybber/HotswapAgentWiki/blob/master/img/NetbeansSetup-02.png)
If you don?t enable this feature, you will need to hotswap changes manually by 

**Maven actions**
If you run your project with a maven action (usually a plugin like maven-jetty-plugin or maven-tomcat-plugin) setup MAVEN_OPTS for an appropriate target.

In the project properties dialog Actions -> Debug project -> Set Properties add Env.MAVEN_OPTS= .. your configuration ?
![](https://github.com/skybber/HotswapAgentWiki/blob/master/img/NetbeansSetup-03.png)

**Setup application server**
Or if you run your application on an application server (Tomcat, JBoss, Glassfish), use Platform VM options.
![](https://github.com/skybber/HotswapAgentWiki/blob/master/img/NetbeansSetup-04.png)

