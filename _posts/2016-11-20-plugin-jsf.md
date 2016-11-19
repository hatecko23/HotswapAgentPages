---
layout: page
title: "JSF Plugin"
date: 2016-11-19 12:45:13
---
Supported Mojarra, MyFaces implementation. Clear resource bundle cache after any *.properties file is changed.

#### Implementation notes:
* Mojarra plugin initialization is triggered after com.sun.faces.config.ConfigManager.initialize() method in servlet classloader.
* MyFaces plugin is triggered in org.apache.myfaces.config.RuntimeConfig constructor

## TODO:
