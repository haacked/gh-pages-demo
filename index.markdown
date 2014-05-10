---
layout: default
---


# {{ site.github.project_tagline }}

This is a demonstration of some of the cool integrations with GitHub that
GitHub Pages provides.

For example, that heading comes from the GitHub repository this demo is
hosted within.

The repository this demo is hosted in is [{{ site.github.repository_url}}]({{ site.github.repository_url}})

```
{% raw %}
<h1>{{ site.github.project_tagline }}</h1>
{% endraw %}
```

<h2>Contributors</h2>
<p>These lovely people have contributed a change to this repository</p>
<ul>
{% for contributor in site.github.contributors %}
  <li>
    <img src="{{ contributor.avatar_url }}" width="32" height="32" /> {{ contributor.login }}
  </li>
{% endfor %}
</ul>

<p>
The code for generating that list is:
</p>

```
{% raw %}
<ul>
{% for contributor in site.github.contributors %}
  <li>
    <img src="{{ contributor.avatar_url }}" width="32" height="32" /> {{ contributor.login }}
  </li>
{% endfor %}
</ul>
{% endraw %}
```

<h2>Repositories</h2>
<p>This is a list of my public repositories</p>
<div>
  {% for repository in site.github.public_repositories %}
    <span>{{ repository.full_name }} </span>
  {% endfor %}
</div>

```
{% raw %}
<div>
  {% for repository in site.github.public_repositories %}
    <span>{{ repository.full_name }} </span>
  {% endfor %}
</div>
{% endraw %}
```

<h2>Members</h2>
<p>This is a list of the members of my "organization". This is probably just me.</p>
<ul>
{% for member in site.github.organization_members %}
  <li>
    <img src="{{ member.avatar_url }}" width="32" height="32" /> {{ member.login }}
  </li>
{% endfor %}
</ul>

```
{% raw %}
<ul>
{% for member in site.github.organization_members %}
  <li>
    <img src="{{ member.avatar_url }}" width="32" height="32" /> {{ member.login }}
  </li>
{% endfor %}
</ul>
{% endraw %}
```