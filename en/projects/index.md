---
layout: page
title: Projects
---

<section class="box special">
  <header class="major">
    <h2>My Projects</h2>
    <p>A List of Projects</p>
  </header>
  <span class="image featured"><img src="/images/pic01.jpg" alt="" /></span>
</section>
<section class="box special features">
  {% assign count = 0 %}
  {% for project in site.data.enprojects %}
  <div class="features-row"> <!-- Row of TWO Items Each -->
  {% assign left = enproject[count] %}
    <section>
      <span class="image featured">
        <img src="/images/projects/{{ left.pic }}">
      </span>
      <h3>{{ left.title }}</h3>
      <p>{{ left.description }}</p>
      <a href="{{ left.link }}" class="button special">Find Out More</a>
    </section>
  {% increment count %} {% if count == site.data.enprojects.size %}
  {% else %} {% assign right = enproject[count] %}
    <section>
      <span class="image featured">
        <img src="/images/projects/{{ right.pic }}">
      </span>
      <h3>{{ right.title }}</h3>
      <p>{{ right.description }}</p>
      <a href="{{ right.link }}" class="button special">Find Out More</a>
    </section>
  {% increment count %}
  {% endif %}
  </div>
  {% endfor %}
</section>
