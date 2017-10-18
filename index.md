---
layout: main
---

<main class="home" id="post" style="max-width:1080px;margin:auto" role="main" itemprop="mainContentOfPage" itemscope="itemscope" itemtype="http://schema.org/Blog">
    <div id="grid" class="row flex-grid articles-list__items row">
    {% for post in site.posts %}
        <!--<article class="box-item" itemscope="itemscope" itemtype="http://schema.org/BlogPosting" itemprop="blogPost">    
            <div class="box-body">
                {% if post.image %}
                    <div class="cover">
                        {% include new-post-tag.html date=post.date %}
                        <a href="{{ post.url | prepend: site.baseurl }}" {%if isnewpost %}class="new-post"{% endif %}>
                            <img src="assets/img/placeholder.png" data-url="{{ post.image }}" class="preload">
                        </a>
                    </div>
                {% endif %}
                <div class="box-info">
                    <meta itemprop="datePublished" content="{{ post.date | date_to_xmlschema }}">
                    <time itemprop="datePublished" datetime="{{ post.date | date_to_xmlschema }}" class="date">
                        {% include date.html date=post.date %}
                    </time>
                    <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">
                        <h2 class="post-title" itemprop="name">
                            {{ post.title }}
                        </h2>
                    </a>
                    <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">
                        <p class="description">{{ post.introduction }}</p>
                    </a>
                    <div class="tags">
                        {% for tag in post.tags %}
                            <a href="{{ site.baseurl}}/tags/#{{tag | slugify }}">{{ tag }}</a>
                        {% endfor %}
                    </div>
                </div>
            </div>
        </article>      -->
        <article class="col">
        {% include minutes-to-read.html %}
            <div class="articles-list__item item case-study"><a href="{{ post.url | prepend: site.baseurl }}" class="articles-list__item-image"
                target="_self"><span class="image-inner">
                <img  class="image preload" data-url="{{ post.image }}" src="assets/img/placeholder.png" draggable="false" alt="img"></span></a>
                <div class="articles-list__item-desc">
                    <a href="{{ post.url | prepend: site.baseurl }}" class="icon bg-color btn" target="_self"><img src="assets/img/icons/case-study.svg" alt="Case Study" draggable="false" width="25"
                    height="25" class="symbol"><img src="assets/img/icons/arrow.svg" alt="View" width="25"
                    height="25" draggable="fase" class="arrow"><span></span></a><a href="{{ post.url | prepend: site.baseurl }}" target="_self">
                <h6 class="color">{{ post.category }}</h6>
                <h3>{{ post.title }}</h3>                                
                </a>
                <ul style="display:flex">
                 {% for tag in post.tags %}
                    <li href="{{ site.baseurl}}/tags/#{{tag | slugify }}"><a href="{{ site.baseurl}}/tags/#{{tag | slugify }}" class="bd-color tag-success-stories" target="_self">{{ tag }}</a></li>
                 {% endfor %}                                    
                </ul>
                </div>
            </div>
        </article>    
    {% endfor %}
    </div>
</main>
