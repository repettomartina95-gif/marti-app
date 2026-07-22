---
layout: default
title: Teaching
permalink: /teaching/
---

{% assign t = site.data.en.teaching %}

<section class="space-y-10">
  <h1 class="my-2 text-3xl md:text-4xl font-semibold tracking-tight text-slate-800">
    {{ t.title }}
  </h1>

  {% for role in t.roles %}
    <div class="space-y-2 pb-6 {% unless forloop.last %}border-b border-slate-200{% endunless %}">
      <h4 class="text-md font-semibold text-slate-800">
        {{ role.position }}
      </h4>
      <p class="text-sm text-slate-600">
        {{ role.location }}
        <span class="text-sky-600">•</span> 
        <span>{{ role.time }}</span>
      </p>
      <ul class="marker:text-sky-600 marker:text-base list-disc ml-6 mt-2 text-slate-700 text-sm space-y-1">
        {% for subject in role.subjects %}
          <li>{{ subject.name }}</li>
        {% endfor %}
      </ul>
    </div>
  {% endfor %}
</section>
