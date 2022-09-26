---
layout: default
title: Frontend
permalink: /frontend/overview
type: pbl
week: 5
---

{% include nav_frontend.html %}

### Frontend Web Development Overview

<div>

    <div style="float: left; margin: 0px 10px 10px 0px;">
        <a href="https://en.wikipedia.org/wiki/Front-end_web_development">
            <img atl="Wikipedia Front-end" src="{{site.baseurl}}/images/html-css-js.jpeg" title=""
            width="200">
        </a>
    </div>
    <div>
        <hr>
        <p>
            Frontend web development is the development of the graphical user interface of a website, through the use of HTML, CSS, and JavaScript, so that users can view and interact with that website.  
            <ul>
                <li>In this class, we will be using <a href="https://github.com/fastai/fastpages"><mark>Fastpages</mark></a> on top of GitHub Pages to maximize our presentations, while minimizing our front-end coding. GitHub Pages deployment is performed through <a href="https://jekyllrb.com/"><mark>Jekyll</mark></a>, which regenerates the website automatically after each commit, tracking can be seen in Actions tab within GitHub.</li>

                <li> HTML generation is performed through <a href="https://shopify.github.io/liquid/basics/introduction/"><mark>Liquid</mark></a>, a template language (similar to Jinja2 or Thymeleaf).</li>

                <li>CSS style layout is provided by using <a href="https://pages.github.com/themes/"><mark>Themes</mark></a> provided through GH Pages. Each page we make we assume the defined theme and insert our HTML fragments, local page style, and local page JavaScript.</li>

                <li><a href="https://www.javascript.com/"><mark>JavaScript</mark></a> enable pages to have actions, fetch content, animate, etc</li> 
            </ul>
        </p>
        <hr>
    </div>

</div>
