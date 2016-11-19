---
layout: default
title: {{ site.github.project_title}}
---


[![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/HotswapProjects/user) [![Build Status](https://travis-ci.org/HotswapProjects/HotswapAgent.svg?branch=master)](https://travis-ci.org/HotswapProjects/HotswapAgent)

Java unlimited runtime class and resource redefinition.

The main purpose of this project is to avoid infamous change->restart + *wait*->check development lifecycle.
Save&Reload during development should be standard and many other languages (including C#) contain this feature.

This project is still in a beta version.

### Easy to start
Download and install latest [DCEVM Java patch](https://github.com/dcevm/dcevm/releases) +
[agent jar](https://github.com/HotswapProjects/HotswapAgent/releases) and launch your application server
with options `-XXaltjvm=dcevm -javaagent:hotswap-agent.jar` to get basic setup. You can attach [agent jar](https://github.com/HotswapProjects/HotswapAgent/releases) to the running JVM using the following example [code snippet](https://gist.github.com/xnike/a268fc209df52bf1bf09a268e97cef53). Optionally add hotswap-agent.properties to your application to configure plugins and agent behaviour.

### Plugins
Each application framework (Spring, Hibernate, Logback, ...) needs special reloading mechanism to keep
up-to-date after class redefinition (e.g. Hibernate configuration reload after new entity class is introduced).
Hotswap agent works as a plugin system and ships preconfigured with all major framework plugins. It is easy
to write your custom plugin even as part of your application.

### Contribute
This project is very complex due to lot of supported frameworks and various versions. Community contribution
is mandatory to keep it alive. You can start by creating a plugin inside your application or by writing an
example/integration test. There is always need for documentation improvement :-). Thank you for any help!

