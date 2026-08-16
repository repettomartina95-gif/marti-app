---
layout: default
title: Home
---

{% assign t = site.data.en %}

<div class="min-h-[60vh] flex flex-col justify-center gap-6">
  <div class="flex flex-col-reverse items-center gap-6 text-center md:flex-row md:items-start md:gap-2 md:text-left">
  <div>
    <div class="my-2 flex flex-wrap items-center gap-4 justify-center md:justify-start">
      <h1 class="text-3xl md:text-4xl font-semibold tracking-tight text-slate-800">
        {{ t.home.title }}
      </h1>
      {% if t.home.job_market %}
      <span aria-hidden="true" class="hidden sm:block h-8 w-px bg-slate-300"></span>
      <span class="text-xs font-semibold uppercase tracking-[0.2em] text-sky-700 whitespace-nowrap">
        {{ t.home.job_market }}
      </span>
      {% endif %}
    </div>
    <p class="text-sm uppercase tracking-[0.2em] text-slate-500">
      {{ t.home.tagline }}
    </p>
      <p class="mt-2 text-sm font-medium text-sky-700">
      {{ t.home.visiting }}
    </p>
    <p class="mt-4 max-w-2xl text-slate-600 leading-relaxed">
      {{ t.home.intro }}
    </p>
  </div>

  <img
    src="{{ '/assets/images/marti.jpg' | relative_url }}"
    class="size-48 shrink-0 rounded-full object-cover"
  />
  </div>
  <div class="flex flex-wrap justify-center gap-3 md:justify-start">
    <a href="{{ '/research/' | relative_url }}"
       class="inline-flex items-center justify-center rounded-full bg-sky-700 px-5 py-2.5 text-sm font-medium text-white hover:bg-sky-800">
      View research
    </a>
    <a href="{{ '/assets/files/CV.pdf' | relative_url }}"
      class="inline-flex items-center justify-center rounded-full border border-slate-300 px-5 py-2.5 text-sm font-medium text-slate-700 hover:bg-slate-100"
      download>
      Download CV
    </a>
  </div>
</div>
