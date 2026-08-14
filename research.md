---
layout: default
title: Research
permalink: /research/
---
{% assign t = site.data.en %}

<section class="space-y-10">

  <header class="space-y-3">
    <h1 class="my-2 text-3xl md:text-4xl font-semibold tracking-tight text-slate-800">
      {{ t.research.title }}
    </h1>
  </header>

  
  <section class="space-y-3">
    <h2 class="text-xl font-semibold text-slate-900">
      {{ t.research.publications.title }}
    </h2>
    <ul class="mt-2 space-y-4 text-slate-800 text-sm leading-relaxed">
      {% for paper in site.data.en.research.publications.papers %}
        <li class="space-y-2 border-l-2 border-sky-600 pl-4">
          <p class="font-semibold text-slate-900">
            {{ paper.name }}
          </p>
          <p class="text-slate-700">
            {{ paper.coauthors }}
          </p>
          <p class="text-slate-600 italic">
            {{ paper.subheading }}
            {% if paper.link %}
              <a href="{{ paper.link }}" class="not-italic ml-3 font-semibold text-sky-700 hover:underline" target="_blank" rel="noopener noreferrer">
                Article Link
              </a>
            {% endif %}
          </p>
          <p class="text-sm text-slate-600 leading-relaxed">
            {{ paper.description }}
          </p>
        </li>
      {% endfor %}
    </ul>
  </section>

  <section class="space-y-3">
    <h2 class="text-xl font-semibold text-slate-900">
      {{ t.research.work_in_progress.title }}
    </h2>
    <ul class="mt-2 space-y-4 text-slate-800 text-sm leading-relaxed">
      {% for paper in site.data.en.research.work_in_progress.papers %}
        <li class="space-y-2 border-l-2 border-sky-600 pl-4">
          <p class="font-semibold text-slate-900">
            {{ paper.name }}
          </p>
          {% if paper.coauthors %}
            <p class="text-slate-700">
              {{ paper.coauthors }}
            </p>
          {% endif %}
          {% if paper.description %}
            <p class="text-sm text-slate-600 leading-relaxed">
              {{ paper.description }}
            </p>
          {% endif %}
        </li>
      {% endfor %}
    </ul>
  </section>

  <section class="space-y-3">
    <h2 class="text-xl font-semibold text-slate-900">
      {{ t.research.other_reports.title }}
    </h2>
    <ul class="marker:text-sky-600 marker:text-base list-disc ml-6 mt-2 text-slate-700 text-sm space-y-1">
      {% for item in site.data.en.research.other_reports.items %}
        <li class="space-y-2 pl-4">
          <p class="text-slate-900">
            {{ item.text }}
            {% if item.link %}
              <a href="{{ item.link }}" class="text-sky-700 hover:underline" target="_blank" rel="noopener noreferrer">
                {{ item.link_text }}
              </a>
            {% endif %}
          </p>
        </li>
      {% endfor %}
    </ul>
  </section>

</section>
