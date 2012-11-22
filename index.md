---
title: Ikbear
description:

layout : page
---

“We shape our tools and afterwards our tools shape us.”---Herbert Marshall McLuhan，1911-1980

很高兴我的个人网站也能够及时更新，希望你会喜欢。 

这是记录我个人思考的地方，我希望能将其维护好。思考是我赖以生存的工具，我希望通过记录思考的方式来将其打造；同时也希望通过这种工具提供些有价值的东西。


### 最近发布的文章

<br>

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>