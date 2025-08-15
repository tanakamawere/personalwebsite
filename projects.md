---
layout: default
title: Projects
permalink: "projects"
---

<div class="container">
    <!-- Hero Section -->
    <div class="row align-items-center py-5 mb-5">
        <div class="col-lg-6">
            <div class="text-center text-lg-start">
                <h1 class="display-4 fw-bold mb-4">My Projects</h1>
                <p class="lead text-muted mb-4">
                    A collection of my work spanning programming projects, businesses, and creative endeavors. 
                    Each project represents a journey of learning, innovation, and problem-solving.
                </p>
                <div class="d-flex flex-wrap gap-2 justify-content-center justify-content-lg-start">
                    <span class="badge bg-primary-subtle text-primary px-3 py-2">Full-Stack Development</span>
                    <span class="badge bg-success-subtle text-success px-3 py-2">Medical Tech</span>
                    <span class="badge bg-info-subtle text-info px-3 py-2">AI & Machine Learning</span>
                    <span class="badge bg-warning-subtle text-warning px-3 py-2">Web Applications</span>
                </div>
            </div>
        </div>
        <div class="col-lg-6 text-center">
            <div class="position-relative">
                <div class="bg-primary bg-opacity-10 rounded-circle d-inline-flex align-items-center justify-content-center" style="width: 200px; height: 200px;">
                    <i class="fas fa-code icon-colour" style="font-size: 4rem;"></i>
                </div>
                <div class="position-absolute top-0 start-100 translate-middle bg-success rounded-circle d-flex align-items-center justify-content-center" style="width: 60px; height: 60px;">
                    <i class="fas fa-lightbulb text-white"></i>
                </div>
                <div class="position-absolute bottom-0 start-0 translate-middle bg-warning rounded-circle d-flex align-items-center justify-content-center" style="width: 50px; height: 50px;">
                    <i class="fas fa-rocket text-white"></i>
                </div>
            </div>
        </div>
    </div>

    <!-- Projects by Category -->
    {% assign categories = site.projects | map: 'category' | uniq | sort %}
    {% for cat in categories %}
        <div class="mb-5">
            <!-- Category Header -->
            <div class="d-flex align-items-center mb-4">
                <div class="flex-shrink-0 me-3">
                    {% if cat == 'Work' %}
                        <div class="bg-primary bg-opacity-10 rounded-circle d-flex align-items-center justify-content-center" style="width: 50px; height: 50px;">
                            <i class="fas fa-briefcase text-primary"></i>
                        </div>
                    {% elsif cat == 'Personal' %}
                        <div class="bg-success bg-opacity-10 rounded-circle d-flex align-items-center justify-content-center" style="width: 50px; height: 50px;">
                            <i class="fas fa-heart text-success"></i>
                        </div>
                    {% elsif cat == 'Open Source' %}
                        <div class="bg-info bg-opacity-10 rounded-circle d-flex align-items-center justify-content-center" style="width: 50px; height: 50px;">
                            <i class="fab fa-github text-info"></i>
                        </div>
                    {% else %}
                        <div class="bg-secondary bg-opacity-10 rounded-circle d-flex align-items-center justify-content-center" style="width: 50px; height: 50px;">
                            <i class="fas fa-folder text-secondary"></i>
                        </div>
                    {% endif %}
                </div>
                <div>
                    <h2 class="h3 fw-bold mb-1">{{ cat }}</h2>
                    <p class="text-muted mb-0">
                        {% if cat == 'Work' %}
                            Professional projects and client work
                        {% elsif cat == 'Personal' %}
                            Side projects and personal experiments
                        {% elsif cat == 'Open Source' %}
                            Community contributions and open source work
                        {% else %}
                            Exploring new technologies and ideas
                        {% endif %}
                    </p>
                </div>
            </div>

            <!-- Projects Grid -->
            <div class="row g-4">
                {% for project in site.projects %}
                    {% if project.category == cat %}
                        {% include projects-control.html %}
                    {% endif %}
                {% endfor %}
            </div>
        </div>
    {% endfor %}

    <!-- Call to Action -->
    <div class="text-center py-5 my-5">
        <div class="bg-light-gray rounded-4 p-5">
            <h3 class="fw-bold mb-3">Interested in Collaborating?</h3>
            <p class="text-muted mb-4">
                I'm always open to discussing new projects, creative ideas, or opportunities to be part of your vision.
            </p>
            <div class="d-flex gap-3 justify-content-center flex-wrap">
                <a href="/about" class="btn btn-primary btn-lg px-4">
                    <i class="fas fa-user me-2"></i>About Me
                </a>
                <a href="mailto:your-email@example.com" class="btn btn-outline-primary btn-lg px-4">
                    <i class="fas fa-envelope me-2"></i>Get In Touch
                </a>
            </div>
        </div>
    </div>
</div>