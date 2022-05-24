---
title: "IT Army of Ukraine"
subtitle: "Analysis of Novice DDOS Tool Users"
excerpt: "This is a small study of characteristics of users of pre-made DDOS tools in the wake of Ukraine’s call to create an ‘IT Army’ to combat disinformation by engaging in ever-changing activities directed through a Telegram channel created for the purpose."
date: 2022-05-12
author: "Kristina Becvar"
draft: false
series:
tags:
categories:
- Projects
- Ukraine
- User Analysis
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
---

#### This is a small study of characteristics of users of pre-made DDOS tools in the wake of Ukraine’s call to create an ‘IT Army’ to combat disinformation by engaging in ever-changing activities directed through a Telegram channel created for the purpose. [^1]

---

## IT Army of Ukraine Basic DDOS User Analysis

### Background

When Russia invaded Ukraine in February 2021, Ukraine’s vice minister of technology called for those with the desire and skill to assist the fight against Russian disinformation. The method of action was to be communicated via a channel on the social media platform “Telegram”, and the title of the group is “IT Army of Ukraine”. The call to join this cause was announced on Twitter, and was amplified by numerous regular and social media platforms.

As this happened during the period of my studies on social data analysis, I joined the group to observe if there was anything to study under this topic. After a couple of days, the leaders of the Telegram channel put a welcome post directing those joining the channel to ways they can contribute based on their knowledge of “hacking” or overall programming knowledge. The primary recommendation to those with no to minimal knowledge of hacking tools was to click on a link to a “DDOS tool” that the user could click on and leave open in their browser that was pre-programmed to a set of Russian media sites that the channel leaders claimed were spreading misinformation about the war.

One thing to note is that upon clicking on the link, a ‘warning’ box popped up for the user that informed them that engaging in assisting in this manner may not be legal in the user’s geographical location. If the user clicks “accept” to that warning, the script begins running.

When exiting the tool, the page GitHub repository link was listed on the bottom of the site. In the corresponding GitHub repository, the person who designed the page had added in a module to track the location of the users who had “accepted” the warning and continued on to use the DDOS tool.

This repository is where I gathered the data for this project, on a daily basis, as of midnight GMT/UTC time.

---

### Hypothesis

I looked at a model where the outcome is the number of DDOS attacks originated from a given country and explanatory variables are WVS activism scores, media coverage, and other controls.

---

## Data

### Telegraph IT Army Channel DDOS Usage

The primary data is the set of observations of users of one novice “hacking tool” to engage in DDOS (denial of service) attacks against Russian targets in March 2022. The data contains a total of users cumulatively for each day of the series March 2 through March 11, and the users represent participants from 98 counties.

### IVS Data

Additional data is from the IVS (Integrated Values Study); a collaboration of the European Values Study and World Values Study.

The European Value Study (EVS) and the World Value Survey (WVS) are two large-scale, cross-national and repeated cross-sectional survey research programs. They include a large number of questions, which have been replicated since the early eighties.

In line with the Memorandum of Understandings, both organizations agreed to cooperate in joint data collection from 2017. EVS has been responsible for planning and conducting surveys in European countries, using the EVS questionnaire and EVS methodological guidelines. WVSA has been responsible for planning and conducting surveys in countries in the world outside Europe, using the WVS questionnaire and WVS methodological guidelines. Five countries (Germany, Romania, Russia, Serbia, and Ukraine) conducted surveys in both waves EVS 2017 and WVS7.

Both organizations developed their draft questionnaires independently. The joint items define the Common Core of both questionnaires. They are marked in yellow in the two Master Questionnaires (EVS2017 MQ and WVS7 MQ).

The EVS archive (GESIS) has been responsible for data archiving and data processing of the European surveys. The WVS archive (JDS Madrid) has been responsible for data archiving and data processing for the non-European surveys and the WVS surveys additionally conducted in Germany, Romania, Russia, Serbia, and Ukraine. Based on the Common EVS/WVS Dictionary agreed by EVS and WVS the Joint EVS/WVS 2017-2021 dataset (Joint EVS/WVS) has been constructed in close collaboration.

The first version of the Joint EVS/WVS includes data and documentation of altogether 81 countries and territories: 35 from the EVS 2017, 51 from the WVS7. Five of these countries (Germany, Romania, Russia, Serbia, and Ukraine) conducted surveys in both waves EVS and WVS.

---

### Preliminary Results

The preliminary analysis of this data did not show any significant correlation between DDOS participants and any of the variables analyzed.

{{< figure src="poster.png" alt="Preliminary Research Presentation" caption="Poster Presentation of Preliminary Research on This Project" >}}

---

### <dfn title="A complete list of citations can be found on the GitHub Page for this project.">Citations</dfn>

A complete list of citations can be found on the GitHub Page for this project.

> ##### Data Survey Citations
>
> EVS (2021): EVS Trend File 1981-2017. GESIS Data Archive, Cologne. ZA7503 Data file Version 2.0.0, doi:10.4232/1.13736.
> 
> Haerpfer, C., Inglehart, R., Moreno, A., Welzel, C., Kizilova, K., Diez-Medrano J., M. Lagos, P. Norris, E. Ponarin & B. Puranen et al. (eds.). 2021. World Values Survey Time-Series (1981-2020) Cross-National Data-Set. Madrid, Spain & Vienna, Austria: JD Systems Institute & WVSA Secretariat. Version 2.0.0, doi:10.14281/18241.15.

---

#### This project will continue in the coming months utilizing new tools as developed in continuing DACSS courses.

[^1]: The work on this project was done as part of the UMass Amherst DACSS Course "Quantitative Data Analysis"" taught by Professor Omer Yalcin.