---
title: Plietsches Tohuus
---

# What is it all about?

In a series of posts we will document our implementation of a smart home (*"plietsches Tohuus"* in Low German).

<ul>
    {% for post in site.posts %}
        <li>
            <a href="{{ post.url }}">{{ post.title }}</a>
        </li>
    {% endfor %}
</ul>
