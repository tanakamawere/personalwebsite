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
    
    {% assign categories = site.projects | map: 'category' | uniq | sort %}
    {% for cat in categories %}
        <div class="container-fluid py-3">
            <h3 class="fw-bold">{{ cat }}</h3>
            <div class="row gx-5">
                {% for project in site.projects %}
                    {% if project.category == cat %}
                        {% include projects-control.html %}
                    {% endif %}
                {% endfor %}
            </div>
        </div>
    {% endfor %}
</div>