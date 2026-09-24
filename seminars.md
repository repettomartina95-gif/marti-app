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

      {% assign completed = block.items | where_exp: "i", "i.upcoming != true" %}
      {% assign upcoming = block.items | where: "upcoming", true %}

      {% if completed.size > 0 %}
        <ul class="mt-3 space-y-3 text-slate-800 text-sm leading-relaxed">
          {% for item in completed %}
            <li class="relative pl-5">
              <span class="absolute left-0 top-2 h-1.5 w-1.5 rounded-full bg-sky-600"></span>
              {% if item.role %}<span class="text-slate-700">{{ item.role }}, </span>{% endif %}<span class="font-semibold text-slate-900">{{ item.name }}</span>{% if item.location and item.location != "" %}<span class="text-slate-600"> • {{ item.location }}</span>{% endif %}
            </li>
          {% endfor %}
        </ul>
      {% endif %}

      {% if upcoming.size > 0 %}
        <div class="mt-4 border-l-2 border-sky-200 pl-4">
          <h3 class="text-xs font-semibold uppercase tracking-wider text-sky-700">Upcoming</h3>
          <ul class="mt-2 space-y-2 text-slate-800 text-sm leading-relaxed">
            {% for item in upcoming %}
              <li class="relative pl-5">
                <span class="absolute left-0 top-2 h-1.5 w-1.5 rounded-full bg-sky-300"></span>
                {% if item.role %}<span class="text-slate-700">{{ item.role }}, </span>{% endif %}<span class="font-semibold text-slate-900">{{ item.name }}</span>{% if item.location and item.location != "" %}<span class="text-slate-600"> • {{ item.location }}</span>{% endif %}
              </li>
            {% endfor %}
          </ul>
        </div>
      {% endif %}
    </section>
  {% endfor %}
</section>
