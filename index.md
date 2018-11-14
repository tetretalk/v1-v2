---
layout: main
---


    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/materialize/1.0.0/css/materialize.min.css">

    <script src="https://cdnjs.cloudflare.com/ajax/libs/materialize/1.0.0/js/materialize.min.js"></script>

      <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
      <link type="text/css" rel="stylesheet" href="css/materialize.min.css"  media="screen,projection"/>

      
      <link type="text/css" rel="stylesheet" href="https://tetretalk.gq/materialize.css"  media="screen,projection"/>
      
<link rel = "stylesheet"
   type = "text/css"
   href = "https://unpkg.com/material-components-web@latest/dist/material-components-web.min.css" />
<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">

<style>
  .brand-logo {
    border-radius: 55px;
}
</style>

<!--JavaScript at end of body for optimized loading-->
      <script type="text/javascript" src="js/materialize.min.js"></script>
<div class="navbar-fixed">
<nav class="nb">
    <div class="nav-wrapper">
      <span class="new badge blue" data-badge-caption="Version 1"></span><a href="/"><img class="brand-logo" src="/favicon.ico" width="64" height="64"></a>
      <ul class="right hide-on-med-and-down">
<li><a href="/"><i class="material-icons left">games</i>Home</a></li>
        <li><a href="/create"><i class="material-icons left">add</i>Submit Game</a></li>
<li><a href="/rules"><i class="material-icons left">block</i>Rules</a></li>
<li><a href="https://discordapp.com/invite/CVBGKh"><i class="material-icons left">forum</i>Discord</a></li>
<li><a><i class="material-icons left">copyright</i>Copyright/Credits</a></li>

      </ul>
    </div>
  </nav>
</div>
<center>
<nav class="ann green"><i class="material-icons left tal">new_releases</i><b>🚀🚀Tetretalk Has Successfully Released!🚀🚀</b><i class="material-icons right tar">new_releases</i></nav>
</center>

<style>
.badge {
  position: absolute;
  top: 20px;
  left: 60px;
}
.ann {
  position: absolute;
  top: 80px;
}
.tal {
  position: absolute;
  top: 5px;
  left: 210px;
}
.tar {
  position: absolute;
  top: 5px;
  right: 210px;
}
.tmr {
  width: 500px;
}
</style>


<main class="home" id="post" role="main" itemprop="mainContentOfPage" itemscope="itemscope" itemtype="http://schema.org/Blog">
    <div id="grid" class="row flex-grid">
    {% for post in site.posts %}
        <article class="box-item" itemscope="itemscope" itemtype="http://schema.org/BlogPosting" itemprop="blogPost">
            <span class="category">
                <a href="{{ site.url }}{{ site.baseurl }}/category/{{ post.category }}">
                    <span>{{ post.category }}</span>
                </a>
            </span>
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
        </article>
    {% endfor %}
    </div>
</main>
