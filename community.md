---
layout: default
title: Community & People
---

## Leaders

<div class="people">
{% for entry in site.data.people %}
    {% assign username = entry[0] %}
    {% assign user = entry[1] %}
    {% if user.roles contains 'leader' %}
        {% include people.html user=user username=username %}
    {% endif %}
{% endfor %}
</div>

## Trainers

<div class="people">
{% for entry in site.data.people %}
    {% assign username = entry[0] %}
    {% assign user = entry[1] %}
    {% if user.roles contains 'trainer' %}
        {% include people.html user=user username=username %}
    {% endif %}
{% endfor %}
</div>

## Everyone

<div class="community">
    {% for user in site.data.people %}
        {% assign username = user[0] %}
        {% assign details = user[1] %}
        <div class="card people-card">
            <div class="card-content">
                <div class="media">
                    <div class="media-left people-card-avatar">
                        <figure class="image is-48x48">
                            <a href="#{{ username }}">
                                <img
                                    class="is-rounded"
                                    src="https://avatars.githubusercontent.com/{{ username }}"
                                    alt="The GitHub avatar of {{ details.name }}"/>
                            </a>
                        </figure>
                    </div>
                </div>
            </div>
        </div>
    {% endfor %}
</div>