---
layout: default
title: "Blog"
---

{% include blog_banner.html %}

<section class="ftco-section bg-light">
  <div class="container">
    <div class="row">
      {% for post in site.posts %}
      <div class="col-md-6 col-lg-4 ftco-animate">
        <div class="blog-entry">
          <a href="{{ post.url }}" class="block-20 d-flex align-items-end" style="background-image: url('assets/img/{{ post.img }}.jpg');">
            <div class="meta-date text-center p-2">
              <span class="day">{{ post.date | date: "%d" }}</span>
              <span class="mos">{{ post.date | date: "%m" }}</span>
              <span class="yr">{{ post.date | date: "%Y" }}</span>
            </div>
          </a>
          <div class="text bg-white p-4">
            <h3 class="heading"><a href="{{ post.url }}">{{ post.title }}</a></h3>
            <p>{{ post.excerpt | strip_html | strip_newlines | truncate: 140 }}</p>
            <div class="d-flex align-items-center mt-4">
              <p class="mb-0"><a href="{{ post.url }}" class="btn btn-primary">Leer más</a></p>
              <p class="ml-auto mb-0">
                <a href="#" class="mr-2">Atenea</a>
              </p>
            </div>
          </div>
        </div>
      </div>
      {% endfor %}
    </div>
  </div>
</section>