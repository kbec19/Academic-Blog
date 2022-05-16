---
author: Kristina Becvar 
categories:
- Projects
- Ukraine
- User Analysis
date: "2022-04-19"
draft: false
excerpt: This is a small study of characteristics of users of pre-made DDOS tools in the wake of Ukraine’s call to create an ‘IT Army’ to combat disinformation by engaging in ever-changing activities directed through a Telegram channel created for the purpose.
layout: single
links:
- icon: door-open
  icon_pack: fas
  name: website
  url: https://kbec19.github.io/it-army/
- icon: github
  icon_pack: fab
  name: code
  url: https://github.com/kbec19/it-army
subtitle: Analysis of Novice DDOS Tool Users
tags:
- hugo-site
title: IT Army of Ukraine
---

### This is a small study of characteristics of users of pre-made DDOS tools in the wake of Ukraine’s call to create an ‘IT Army’ to combat disinformation by engaging in ever-changing activities directed through a Telegram channel created for the purpose.

*— [IT Army Project GitHub Page](https://kbec19.github.io/it-army/)*

---

# IT Army of Ukraine Basic DDOS User Analysis

## Background

When Russia invaded Ukraine in February 2021, Ukraine’s vice minister of technology called for those with the desire and skill to assist the fight against Russian disinformation. The method of action was to be communicated via a channel on the social media platform “Telegram”, and the title of the group is “IT Army of Ukraine”. The call to join this cause was announced on Twitter, and was amplified by numerous regular and social media platforms.

As this happened during the period of my studies on social data analysis, I joined the group to observe if there was anything to study under this topic. After a couple of days, the leaders of the Telegram channel put a welcome post directing those joining the channel to ways they can contribute based on their knowledge of “hacking” or overall programming knowledge. The primary recommendation to those with no to minimal knowledge of hacking tools was to click on a link to a “DDOS tool” that the user could click on and leave open in their browser that was pre-programmed to a set of Russian media sites that the channel leaders claimed were spreading misinformation about the war.

One thing to note is that upon clicking on the link, a ‘warning’ box popped up for the user that informed them that engaging in assisting in this manner may not be legal in the user’s geographical location. If the user clicks “accept” to that warning, the script begins running.

When exiting the tool, the page GitHub repository link was listed on the bottom of the site. In the corresponding GitHub repository, the person who designed the page had added in a module to track the location of the users who had “accepted” the warning and continued on to use the DDOS tool.

This repository is where I gathered the data for this project, on a daily basis, as of midnight GMT/UTC time.

## Hypothesis

I am looking at a model where the outcome is the number of DDOS attacks originated from a given country and explanatory variables are WVS activism scores, media coverage, and other controls.

---

### <dfn title="A complete list of citations can be found on the GitHub Page for this project.">Citations</dfn>

A complete list of citations can be found on the GitHub Page for this project.

> ##### Data Survey Citations
>
> EVS (2021): EVS Trend File 1981-2017. GESIS Data Archive, Cologne. ZA7503 Data file Version 2.0.0, doi:10.4232/1.13736.
> 
> Haerpfer, C., Inglehart, R., Moreno, A., Welzel, C., Kizilova, K., Diez-Medrano J., M. Lagos, P. Norris, E. Ponarin & B. Puranen et al. (eds.). 2021. World Values Survey Time-Series (1981-2020) Cross-National Data-Set. Madrid, Spain & Vienna, Austria: JD Systems Institute & WVSA Secretariat. Version 2.0.0, doi:10.14281/18241.15.

---

[^1]: The preliminary work on this project was done as part of the UMass Amherst DACSS Course "Quantitative Data Analysis"" taught by Professor Omer Yalcin: [IT Army Analysis Project GitHub Page](https://kbec19.github.io/it-army/)