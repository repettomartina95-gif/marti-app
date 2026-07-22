---
layout: default
title: Seminars & Conferences
permalink: /seminars/
---

{% assign seminars = site.data.en.seminars.years %}

<section class="space-y-8">
  <header>
    <h1 class="my-2 text-3xl md:text-4xl font-semibold tracking-tight text-slate-800">
      Seminars & Conferences
    </h1>
  </header>

  {% for block in seminars %}
    <section class="space-y-3">
      <h2 class="text-xl font-semibold text-slate-900">
        {{ block.year }}
      </h2>
      <ul class="mt-3 space-y-3 text-slate-800 text-sm leading-relaxed">
        {% for item in block.items %}
          <li class="relative pl-5">
            <span class="absolute left-0 top-2 h-1.5 w-1.5 rounded-full bg-sky-600"></span>
            <span class="font-semibold text-slate-900">{{ item.name }}</span>
            <span class="text-slate-600"> • {{ item.location }}</span>
          </li>
        {% endfor %}
      </ul>
    </section>
  {% endfor %}
</section>
