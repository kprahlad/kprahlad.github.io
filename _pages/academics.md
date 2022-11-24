---
layout: page
title: Academics
permalink: academics.html
---

![]({{site.baseurl}}/images/DSC_0342.jpg)*Tiger paw prints at Ranthambore. Spring, 2018.*

## An Academic History

I'm currently enrolled as a PhD student in the Applied Mathematics amd Statistics Department at SUNY, Stony Brook. In 2022, I completed a 5-year Integrated MSc. course at NISER, Bhubaneswar in mathematics with a minor in computer science. I was graciously supported by the Department of  Science and Technology through the INSPIRE SHE fellowship throughout my studies at NISER. My research  interests lie in the realm of theoretical computer science -  specifically, I'm working on problems in computational geometry, graph  theory, and parameterized complexity. I've previously worked on automata theory, cryptographic applications of cellular automata, and optimization.

Here is a <a href = "{{site.baseurl}}/documents/CV_Prahlad.pdf" download>PDF of my CV</a> (updated: November 20, 2022).

I've listed my publications, talks, academic reports, and some random problems below. Click on the title to head to the blog post on the topic and the <i class="fas fa-caret-square-down"></i> icon to read its excerpt.

## Publications

Here is a list of my publications:

<ul>
    {% for post in site.tags.Publications %}
        <li><a href = "{{post.url}}">{{post.title}}</a> 
            <a onclick="myCollapse('{{post.title}}')" style="cursor:pointer"><i aria-hidden="true" id="{{post.title}}-but" class="fas fa-caret-square-down"></i></a><br>
            <div id="{{post.title}}" class="w3-container w3-hide w3-margin-bottom w3-leftbar">
                {{post.excerpt}}
            </div>
        </li>
    {% endfor %}
</ul>

## Talks

Here are slides and recordings (if available) of my talks:

<ul>
    {% for post in site.tags.Presentations %}
        <li><a href = "{{post.url}}">{{post.title}}</a>
            <a onclick="myCollapse('{{post.title}}')" style="cursor:pointer"><i aria-hidden="true" id="{{post.title}}-but" class="fas fa-caret-square-down"></i></a><br>
            <div id="{{post.title}}" class="w3-container w3-hide w3-margin-bottom w3-leftbar">
                {{post.excerpt}}
            </div>
        </li>
    {% endfor %}
</ul>

## Reports

Here is a list of reports that I have submitted as part of my coursework or at the end of an internship:

<ul>
    {% for post in site.tags.Reports %}
        <li><a href = "{{post.url}}">{{post.title}}</a>
            <a onclick="myCollapse('{{post.title}}')" style="cursor:pointer"><i aria-hidden="true" id="{{post.title}}-but" class="fas fa-caret-square-down"></i></a><br>
            <div id="{{post.title}}" class="w3-container w3-hide w3-margin-bottom w3-leftbar">
                {{post.excerpt}}
            </div>
        </li>
    {% endfor %}
</ul>

## Random Problems

Here is a list of what I consider to be small,  interesting problems that I have managed to solve:

<ul>
    {% for post in site.tags.Problems %}
        <li><a href = "{{post.url}}">{{post.title}}</a>
            <a onclick="myCollapse('{{post.title}}')" style="cursor:pointer"><i aria-hidden="true" id="{{post.title}}-but" class="fas fa-caret-square-down"></i></a><br>
            <div id="{{post.title}}" class="w3-container w3-hide w3-margin-bottom w3-leftbar">
                {{post.excerpt}}
            </div>
        </li>
    {% endfor %}
</ul>