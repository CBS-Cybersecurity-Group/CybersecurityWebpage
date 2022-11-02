---
title: Our amazing team
subtitle: Collaboration between students and academic professionals.
description: Presenting the team
featured_image: /images/demo/team.jpg
---

<head>
	<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.3.1/dist/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
	<link rel="stylesheet" href="{{ '/css/style.css' | relative_url }}">
</head>


<div class="container">
    <div class="row">
        {% for member in site.data.settings.people %}
        <div class="col-sm-4">
            <div class="team-member m-4">
                <img src="images/team/{{ member.pic }}.jpg" class="img-responsive rounded-circle" alt="">
                <h4 class="mt-3 text-center">{{ member.name }}</h4>
                <p class="text-muted text-center">{{ member.position }}</p>
                <ul class="list-inline social-buttons text-center">
                    {% for network in member.social %}
                    <li class="list-inline-item">
                        <a href="{{ network.url }}">
                            <i class="fab fa-{{ network.title }}"></i>
                        </a>
                    </li>
                    {% endfor %}

                </ul>
            </div>
        </div>
        {% endfor %}
    </div>
</div>
