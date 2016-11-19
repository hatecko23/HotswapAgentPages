---
layout: page
title: "JavaBeans Plugin"
date: 2016-11-19 12:45:13
---
Solves purging Introspector cache in appropriate thread groups for all particular plugins.

#### Implementation notes:
Cache cleanup is triggered on any class redefinition.

