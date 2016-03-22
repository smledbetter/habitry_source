---
layout: article
title: Habit Templates
date: 2016-03-19T15:02:52-07:00
permalink: /habits/
modified:
excerpt: "I'm an excerpt"
image:
  feature:
  teaser:
  thumb:
ads: false
---
{{ page.excerpt | markdownify }}


## Habits
These are the habits that make any Habitry Implemtation run more smoothly.

<div class="row" style="overflow:auto;margin-bottom:2em;">
<h4 style="float: left;margin:.6rem;">Skills</h4><div id="filters" class="button-group filters-button-group">
 <label>
   <input type="radio" name="button-group" data-filter="*" checked>
   <span class="button-group-item">All</span>
 </label>
  <label>
    <input type="radio" name="button-group" data-filter=".eating">
    <span class="button-group-item">Eating</span>
  </label>
  <label>
    <input type="radio" name="button-group" data-filter=".sleeping">
    <span class="button-group-item">Sleeping</span>
  </label>
  <label>
    <input type="radio" name="button-group" data-filter=".moving">
    <span class="button-group-item">Moving</span>
  </label>
  <label>
    <input type="radio" name="button-group" data-filter=".mindset">
    <span class="button-group-item">Mindset</span>
  </label>
  <label>
    <input type="radio" name="button-group" data-filter=".motivating">
    <span class="button-group-item">Motivating Others</span>
  </label>
</div>
</div>

<div class="grid-items">
{% for habits in site.habits %}
<a href="{{ habits.url }}" class="grid-item grid-item-color-{{ habits.level }} {{ habits.skills | join: ' ' }}">
<h1 class="flex-title">{{ habits.title }}</h1>
    <p>{{ habits.exerpt }}</p>
</a>
{% endfor %}
</div>

