---
layout: post
title: Vim cheat sheet
tagline: completely logical use of the keyboard...
description: "A list of commands and handy functions I come across while using vim"
category: 
tags: [vim, commands, cheat sheet]
---
{% include JB/setup %}

##Deleting/Replacing text

|              |                            |
|--------------|----------------------------|
|`c`             | delete plus insert       |
|`d`             | delete                   |
|`d$`            | delete to end of line    |
|`dt<character>` | delete until 'character' |
|`diw`           | Delete inside word       |
|`di<symbol>`    | Delete inside symbol     |
|`diw`||
|`da`||

##Navigation

|             |                             |
|-------------|-----------------------------|
|`_` | Beginning of line without insert     |
|`I` | Beginning of line with insert        |
|`$` | End of line without insert           |
|`A` | End of line with insert              |
