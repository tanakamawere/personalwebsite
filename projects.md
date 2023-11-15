---
layout: default
title: Projects
permalink: "projects"
---

<div class="px-5 container rounded-3">
    <div class="container-fluid py-5">
        <h2 class="display-6 fw-bold">Projects</h2>
        <p class="col-md-8 fs-6">
            The programs I am working on ranging from programming projects, businesses, events and everything else that makes sense to put under this heading
        </p>
    </div>
    <div class="row gx-5">
        {% for project in site.projects %} 
            {% include projects-control.html %}
        {% endfor %}
    </div>
</div>