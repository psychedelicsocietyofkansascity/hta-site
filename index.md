---
layout: splash
title: "Welcome to Our Organization"
permalink: /
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/hero-image.jpg
  actions:
    - label: "Learn More"
      url: "/about/"
      class: "btn btn--primary"
---

The Heartland Transpersonal Alliance is a non-profit organization committed to fostering community, education, harm reduction, and integration around the safe, responsible exploration of consciousness. We believe in creating supportive, evidence-based pathways for personal growth and collective well-being. By bringing together professionals, educators, and curious individuals, we aim to expand understanding, reduce stigma, and promote transformative experiences that honor both individual and community needs.

<!-- Insert some post listings below the splash content -->

{% assign recent_posts = site.posts | sort: "date" | reverse %}
<section class="posts-preview">
  <h2>Latest News</h2>
  <ul>
    {% for post in recent_posts limit:3 %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a> <br>
        <small>{{ post.date | date_to_string }}</small>
      </li>
    {% endfor %}
  </ul>
</section>
