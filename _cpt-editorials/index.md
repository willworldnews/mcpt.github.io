---
layout: default
title: CPT Problem Editorials
description: Editorials to practice problems.
permalink: /cpt-editorials/
---

{% assign contests = site.cpt-editorials | group_by: 'contest' %}

# JDCC

---

## 2015--2016
<div class="page-listing-container">
	{% for contest in contests %}
		{% if contest.name == "jdcc2015" %}
			{% assign rounds = contest.items | sort: 'round' | group_by: 'round-title' %}
			{% for round in rounds %}
				<div class="page-listing">
					<h3>{{ round.name | capitalize }}</h3>
					{% assign problems = round.items | sort: 'difficulty' %}
					{% for problem in problems %}
						<a href="{{ problem.url }}">{{ problem.difficulty | upcase }}. {{ problem.title }}</a><br>
					{% endfor %}
				</div>
			{% endfor %}
		{% endif %}
	{% endfor %}
</div>

## 2016--2017
<div class="page-listing-container">
	{% for contest in contests %}
		{% if contest.name == "jdcc2016" %}
			{% assign rounds = contest.items | sort: 'round' | group_by: 'round-title' %}
			{% for round in rounds %}
				<div class="page-listing">
					<h3>{{ round.name | capitalize }}</h3>
					{% assign problems = round.items | sort: 'difficulty' %}
					{% for problem in problems %}
						<a href="{{ problem.url }}">{{ problem.difficulty | upcase }}. {{ problem.title }}</a><br>
					{% endfor %}
				</div>
			{% endfor %}
		{% endif %}
	{% endfor %}
</div>
