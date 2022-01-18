---
layout: page
title: Personal
permalink: personal.html
---

![]({{site.baseurl}}/images/DSC_0256.jpg)*Sandakphu, as seen from Kalipokhri. March, 2020.*

Growing up, I played a bunch of sports: cricket, football, and volleyball to some success; table tennis, basketball, and chess for the fun of it. I caught the running bug in late 2019 (after my [disastrous trekking experience]({{ site.baseurl }}{% post_url 2020-08-01-Sandakphu-A-Prologue %})) and have been trying to keep it going through the pandemic. I am not very good at it, but boy do I enjoy a run. My short-term running goal is to get back to half-marathon shape but I do hope to run a marathon in the future!

Apart from sports, I enjoy hiking (2020 was a *terrible* time to pick up this hobby), portrait photography, and classical (Carnatic) music - [here](https://www.youtube.com/watch?v=o55TExI7Dbc){:target="_blank"} [are](https://youtu.be/iQTs7PSnX3k){:target="_blank"} [some](https://www.youtube.com/watch?v=yqvDbr4snIQ){:target="_blank"} [of](https://www.youtube.com/watch?v=TqsOCgWskDY){:target="_blank"} [my](https://www.youtube.com/watch?v=r5hSMSpb1Qs){:target="_blank"} [favourite](https://www.youtube.com/watch?v=YZksCuzV59E){:target="_blank"} [songs](https://www.youtube.com/watch?v=Go-mAJpH6_w){:target="_blank"}. I sketch and read books irregularly (I really should do more of them).

I've listed my posts on running, trekking, and other miscellaneous stuff below. Click on the title to head to the blog post on the topic and the <i class="fas fa-caret-square-down"></i> icon to read its excerpt.

## Running

I hope to maintain a collection of my race reports and training blocks here:

<ul>
    {% for post in site.tags.Running %}
        <li><a href = "{{post.url}}">{{post.title}}</a>
			<a onclick="myCollapse('{{post.title}}')" style="cursor:pointer"><i aria-hidden="true" id="{{post.title}}-but" class="fas fa-caret-square-down"></i></a><br>
            <div id="{{post.title}}" class="w3-container w3-hide w3-margin-bottom w3-leftbar">
                {{post.excerpt}}
            </div>
		</li>
    {% endfor %}
</ul>

## Trekking and Hiking

I want to document my treks and hikes here:

<ul>
    {% for post in site.tags.Trekking %}
        <li><a href = "{{post.url}}">{{post.title}}</a>
			<a onclick="myCollapse('{{post.title}}')" style="cursor:pointer"><i aria-hidden="true" id="{{post.title}}-but" class="fas fa-caret-square-down"></i></a><br>
            <div id="{{post.title}}" class="w3-container w3-hide w3-margin-bottom w3-leftbar">
                {{post.excerpt}}
            </div>
		</li>
    {% endfor %}
</ul>

## Miscellaneous

I doubt I will write about much else, but if I do, it shall go here:

<ul>
    {% for post in site.tags.Misc %}
        <li><a href = "{{post.url}}">{{post.title}}</a>
			<a onclick="myCollapse('{{post.title}}')" style="cursor:pointer"><i aria-hidden="true" id="{{post.title}}-but" class="fas fa-caret-square-down"></i></a><br>
            <div id="{{post.title}}" class="w3-container w3-hide w3-margin-bottom w3-leftbar">
                {{post.excerpt}}
            </div>
		</li>
    {% endfor %}
</ul>