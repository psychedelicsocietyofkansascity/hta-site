---
layout: splash
title: "Welcome to Our Organization"
permalink: /
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/hero-image.jpg
  actions:
    - label: "Donate"
      url: "/donate/"
      class: "btn btn--primary"
---

Welcome to our site! We’re dedicated to...

<!-- Insert some post listings below the splash content -->

{% assign recent_posts = site.posts | sort: "date" | reverse %}
<section class="posts-preview">
  <h2>Latest News</h2>
  <ul>
    {% for post in recent_posts limit:3 %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a> <br>
        <small>{{ post.date | date_to_string }}</small>
      </li>
    {% endfor %}
  </ul>
</section>
