---
layout: default
title: "Wang Ruijie's Homepage"
---

<main role="main" class="container-sm" style="max-width: 1080px">
    <div class="row">
        <div class="col">
            <p class="h1 mt-5 page-title">
                <img class="profile-img-small d-md-none" src="{{ '/assets/profile.jpg' | relative_url }}" />
                <img class="chinese-name-img" src="{{ '/assets/Chinese Name.png' | relative_url }}" />
            </p>
            <p class="h4 section-title" style="clear: right">❈ About Me</p>
            {% capture bio %}{% include bio.md %}{% endcapture %}
            <p>{{ bio | markdownify }}</p>
            <a href="mailto:ruijie.wang@connect.polyu.hk">Email</a> /  
                 <a href="https://www.linkedin.com/in/ruijie-wang-780406260/">LinkedIn</a> / <a href="https://github.com/WANGaRuijie">GitHub</a> /
            <a href="{{ '/Curriculum-Vitae-Wang-Ruijie.pdf' | relative_url }}">Curriculum Vitae</a>
        </div>
        <div class="col-auto d-none d-md-block">
            <img class="profile-img" src="{{ '/assets/profile.jpg' | relative_url }}" />
        </div>
    </div>
    {% comment %}
    <div class="row">
        <div class="col">
            <p class="h4 section-title">Publications <span class="h6">(*: equal contribution)</span></p>
            <div class="container-fluid" style="padding: 0;">
                {% assign sorted_publications = site.publications | sort:"date" %}
                {% for publication in sorted_publications reversed %}
                <div class="row" style="padding: 0.25rem 0">
                    <div class="col">
                        <p class="h5 publication-title">{{ publication.title }}</p>
                        <span class="publication-authors">{{publication.authors | markdownify}}</span>
                        {% if publication.venue %}
                            <span class="publication-venue">{{publication.venue | markdownify}}</span>
                        {% endif %}
                        <div class="publication-excerpt" style="display: none">{{publication.excerpt | markdownify}}</div>
                        <!-- <p>{{ publication.content }}</p> -->
                        {% if publication.paper_url %}
                        <p class="publication-links"> <a href="{{publication.paper_url}}">Paper</a> 
                        {% if publication.blog_url %}/ <a href="{{publication.blog_url}}">Blog Post</a>{% endif %} 
                        {% if publication.project_page_url %}/ <a href="{{publication.project_page_url}}">Project Page</a>{% endif %} 
                        {% if publication.demo_url %}/ <a href="{{publication.demo_url}}">Demo</a>{% endif %} 
                        {% if publication.video_url %}/ <a href="{{publication.video_url}}">Video</a>{% endif %} 
                        {% if publication.demo_video_url %}/ <a href="{{publication.demo_video_url}}">Demo Video</a>{% endif %} 
                        {% if publication.code_url %}/ <a href="{{publication.code_url}}">Code</a>{% endif %} 
                        {% if publication.poster %}/ <a href="{{'/assets/posters/' | append: publication.poster | relative_url }}">Poster</a>{% endif %} 
                        {% if publication.bibtex_url %}/ <a href="{{publication.bibtex_url}}">BibTex</a>{% endif %} 
                        {% if publication.excerpt %}/ <a href="" class="tldr_btn" role="button">TL;DR</a>{% endif %} 
                        </p>
                        {% endif %}
                    </div>
                    {% if publication.cover_image %}
                    <div class="col-5 d-none d-md-block align-self-center">
                        <img class="cover-image" src="{{'/assets/cover_images/' | append: publication.cover_image | relative_url }}" />
                    </div>
                    {% endif %}
                </div>
                {% endfor %}
            </div>
        </div>
    </div>
    <div class="row">
        <div class="col">
            <p class="h4 section-title">Academic Services</p>
            <p>
                Reviewer for CVPR/ECCV/ICCV/NeurIPS
            </p>
        </div>
    </div>
    <div class="row">
        <div class="col">
            <p class="h4 section-title">Side Projects</p>
            <p><a href="https://github.com/TonyLianLong/stable-diffusion-xl-demo">Stable Diffusion XL Demo WebUI</a>: A gradio-based WebUI that allows playing around with <a href="https://arxiv.org/abs/2307.01952">SDXL</a> locally and on Colab for free. <a target="_blank" href="https://colab.research.google.com/github/TonyLianLong/stable-diffusion-xl-demo/blob/main/Stable_Diffusion_XL_Demo.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a></p>
            <p><a href="https://github.com/TonyLianLong/AnimeGAN.js">AnimeGAN.js</a>: An implementation of AnimeGAN, which converts photos to anime style online, with <a href="https://github.com/tensorflow/tfjs">tf.js</a>.</p>
            <p><a href="https://github.com/TonyLianLong/Rainbow">Rainbow</a>: An implementation of Rainbow algorithm with <a href="https://github.com/PaddlePaddle/PARL">PARL</a> reinforcement learning framework.</p>
        </div>
    </div>
    {% endcomment %}
</main>

<footer class="footer">
    <div class="container-sm">
        <div class="row justify-content-center"> <!-- Bootstrap's class for centering the content -->
            <div class="col text-center" style="margin-bottom: 15px;"> <!-- Use margin-bottom to create space between the text and the globe -->
                Since 2 June 2024. Based on <a href="https://github.com/TonyLianLong/websitev2"> the remodeled LaTeX-style template.</a><br />
            </div>
        </div>
        <div class="row justify-content-center"> <!-- Create another row for the globe and use Bootstrap's class for centering the content -->
            <div class="col text-center">
                <div class="statics" style="width:100px; height:100px; margin: auto;"> <!-- Add margin:auto to center the globe -->
                    <script type="text/javascript" id="clstr_globe" src="//clustrmaps.com/globe.js?d=9jCt5iZiY6zXourr8DKBF30cXTHyY5UMcQh9rnlozxA"></script>
                </div>
            </div>
        </div>
    </div>
</footer>
