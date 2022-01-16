---
layout: page
title: Academics
permalink: academics.html
---

![]({{site.baseurl}}/images/DSC_0342.jpg)*Tiger paw prints at Ranthambore. Spring, 2018.*

## An Academic History

I'm currently enrolled in a 5-year Int. MSc.  course at NISER, Bhubaneswar and am majoring in mathematics with a minor in computer science. My study here is supported by the Department of  Science and Technology through the INSPIRE SHE fellowship. My research  interests lie in the realm of theoretical computer science -  specifically, I'm working on problems in computational geometry, graph  theory, and parameterized complexity. I've previously worked on automata theory, cryptographic applications of cellular automata, and optimization. I presented my  first publication titled *"One-Sided Discrete Terrain Guarding and Chordal Graphs"* at CALDAM 2021. 

Here is a <a href = "{{site.baseurl}}/documents/CV_Prahlad.pdf" download>PDF of my CV</a> (updated: January 14, 2022).

## Publications

Here is a list of my publications:

<ul>
    {% for post in site.tags.Publications %}
        <li><a href = "{{post.url}}">{{post.title}}</a>: {{post.excerpt}}</li>
    {% endfor %}
</ul>

## Reports

Here is a list of reports that I have submitted as part of my coursework or at the end of an internship:

<ul>
    {% for post in site.tags.Reports %}
        <li><a href = "{{post.url}}">{{post.title}}</a></li>
    {% endfor %}
</ul>

## Random Problems

Here is a list of what I consider to be small,  interesting problems that I have managed to solve:

<ul>
    {% for post in site.tags.Problems %}
        <li><a href = "{{post.url}}">{{post.title}}</a></li>
    {% endfor %}
</ul>