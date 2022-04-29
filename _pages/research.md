---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

<style>
    .mr-1 {
        margin-right: 8px;
    }
    .list_item {
        margin-bottom: 16px;
    }
    .list_item a.downloadable-items {
        #display: flex;
        align-items: baseline;
    }
    .list_item p {
        margin: 0;
    }
    .list_item .venue-year {
        font-style: italic;
    }
    span.own-name {
        text-decoration: underline;
    }
</style>

<h2>Helloworld</h2>

<ol>
{% for post in site.research reversed %}
    <li class="list_item">
        <p>{{post.title}}</p>
        <p>{{ pub.author }}</p>
        <p>{{post.author}}</p>
        <p class="venue-year">{{post.venue}} ({{post.year}})</p>
            {% if post.paperurl %}
                <a href="{{post.paperurl}}" class="downloadable-items">
                    <i class="fas fa-file mr-1" aria-hidden="true"></i>
                    <span style="text-decoration: underline">Paper</span>
                </a>
            {% endif %}
            {% if post.extendedurl %}
                <a href="{{post.extendedurl}}" class="downloadable-items">
                    <i class="fas fa-file mr-1" aria-hidden="true"></i>
                    <span style="text-decoration: underline">Extended paper</span>
                </a>
            {% endif %}
            {% if post.codeurl %}
                <a href="{{post.codeurl}}" class="downloadable-items">
                    <i class="fab fa-fw fa-github mr-1" aria-hidden="true"></i>
                    <span style="text-decoration: underline">Artifact</span>
                </a>
            {% endif %}
            {% if post.slidesurl %}
                <a href="{{post.slidesurl}}" class="downloadable-items">
                    <i class="fas fa-desktop mr-1" aria-hidden="true"></i>
                    <span style="text-decoration: underline">Slides</span>
                </a>
            {% endif %}
            {% if post.videourl %}
                <a href="{{post.videourl}}" class="downloadable-items">
                    <i class="fas fa-video mr-1" aria-hidden="true"></i>
                    <span style="text-decoration: underline">Video</span>
                </a>
            {% endif %}
    </li>
{% endfor %}

</ol>