---
title: "Grateful Network"
subtitle: "A social network analysis of the song co-writing network of original Grateful Dead songs."
excerpt: "I originally started this network as a practice skeleton to build a co-authorship network of New York Times correspondents for another project. But since I have a relatively unreasonable amount of knowledge of Grateful Dead music and history, it just made sense to keep the project alive and growing."
date: 2022-04-20
author: "Kristina Becvar"
draft: false
featured: true
series:
tags:
categories:
- Projects
- Networks
- Grateful Dead
- Music
layout: single
links:
- icon: door-open
  icon_pack: fas
  name: website
  url: http://gratefulnetwork.live/
- icon: github
  icon_pack: fab
  name: github
  url: https://github.com/kbec19/NYT-Analysis
---

#### [Grateful Network](https://github.com/kbec19/Grateful-Network) is the first in a series of repositories built for social network analysis of the Grateful Dead culture and music world. [^1]

![](network.png)

---

### Structure

The data for this project consists of working data in different formats that can lead to the creation of a reproducable network.

There are 26 songwriters that contributed to the original songs played over the course of the Grateful Dead touring history. This is the starting point for my data gathering.

There is always room for competing opinions when it comes to any aspect of the Grateful Dead - but my current working total of original songs represented in this data is 181* songs. There is room for future analysis into whether a "reprise" counts as another song, whether a "jam" of some type has an official or unofficial name, and much more.

There is also information that represents the point of view of multiple archivists in tallying the number of times each of the songs was played live in the 30 year touring life of the Grateful Dead, including my own.

More information to come as this project is developed!

Currently, the GitHub repository contains clean data in various formats as well as scripts for the creation of igraph and statnet network objects.

---

### Current Research

After creating networks using both igraph and statnet, it became clear that it is probable that it is not Jerry Garcia, but Bob Weir, that is the central figure in the Grateful Dead songwriting network. Although the igraph evaluation determined degree centrality higher for Jerry Garcia, even in igraph, Bob Weir had more centrality by every other measure.  In the statnet evaluation, Weir held the mostconsistently strong centrality of any member, including
Jerry Garcia.

Summary presentation of my initial research:

{{< figure src="poster.png" alt="Preliminary Research Presentation" caption="Poster Presentation of Preliminary Research on This Project" >}}

---

### Inspiration, Sources, and Citations

Citations:

*Allan, Alex; Grateful Dead Lyric & Song Finder: https://whitegum.com/~acsa/intro.htm*

*ASCAP. 18 March 2022.*

*Dodd, David; The Annotated Grateful Dead Lyrics: http://artsites.ucsc.edu/gdead/agdl/*

*Schofield, Matt; The Grateful Dead Family Discography: http://www.deaddisc.com/*

*This information is intended for private research only, and not for any commercial use. Original Grateful Dead songs are ©copyright Ice Nine Music*

---

#### This project will continue in the coming months utilizing new tools as developed in continuing DACSS courses.

[^1]: The preliminary work on this project was done as part of the UMass Amherst DACSS Course "Social and Network Analysis"," taught by Professor Meredith Rolfe.
