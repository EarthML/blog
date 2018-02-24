---
layout: ReadArticle
title: Create your own ARM template DSL
subtitle: Learn hwo to create a DSL running on dotnet core
description: In this article you will be seeing how I created a DSL similar to the ARM templates, the motivation for doing this and how I used it for my Docker Pipelines project.
date: 2018-02-24 3:07 AM
alias: /2018/02/24/markdown-blogging-on-aspnet-core/
author:
  name: Poul K. Sørensen
  mail: poul@earthml.com
  url: https://twitter.com/pksorensen
  avatar: https://s.gravatar.com/avatar/9003d0ada00ae43a199d7a5fa1be7714?s=80
design:
  bg_color: #0D3483
tags:
- Docker Pipelines
- AspNet core
---

- [ ] Prof read

# Create your own ARM template DSL

In the past I been asking abit on twitter and then at Azure Saturday 2017 here in copenhagen, i had the chance to talk abit with [Ryan Jones](https://twitter.com/rjmax) but ultimately the answer is no. The ARM parsing code is not avaible as opensource. In the same timeframe i also created some really naive code to do some of the stuff that ARM templates could do with variables and functions. 

https://twitter.com/pksorensen/status/956321593353035776
https://twitter.com/pksorensen/status/863705160052334592
https://twitter.com/pksorensen/status/673155680333901824

Knowing what i know today, i wish that i payed more attention in the compiler classes at uni - because what i really needed was the right search words on google about creating a DSL. So after finding the right resources, it took a few hours to get to the first prototype of my own DSL.

## building on top of JSON

Inspired by ARM (Azure Resource Manager) i also wanted to define my language build ontop of JSON. So having a declarative language where elements within the json document could be computed by use of functions and references to other parts of the document.



