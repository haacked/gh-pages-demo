---
layout: default
---

{{ site.github.project_tagline }}

This is a demonstration of some of the cool integrations with GitHub that
GitHub Pages provides.

For example, that heading comes from the GitHub repository this demo is
hosted within.

```
{% raw %}
<h1>{{ site.github.project_tagline }}</h1>
{% endraw %}
```

The repository this demo is hosted in is [{{ site.github.repository_url}}]({{ site.github.repository_url}})

## Contributors

These lovely people have contributed a change to this repository. If you want to see yourself in this list, send me a pull request. Go to the bottom for a real simple way to help.

<ul>
{% for contributor in site.github.contributors %}
  <li>
    <img src="{{ contributor.avatar_url }}" width="32" height="32" /> {{ contributor.login }}
  </li>
{% endfor %}
</ul>

The code for generating that list is:

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

## Repositories

This is a list of my public repositories

<ul>
  {% for repository in site.github.public_repositories %}
    <li>{{ repository.full_name }} </li>
  {% endfor %}
</ul>

```
{% raw %}
<ul>
  {% for repository in site.github.public_repositories %}
    <li>{{ repository.full_name }} </li>
  {% endfor %}
</li>
{% endraw %}
```

## Members

This is a list of the members of my "organization". This is probably just me.

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

## Help me fix this page up

### CSS Help
If you want to see yourself in this list I could use some help throwing some [simple CSS styles in the default layout]({{ site.github.repository_url}}/edit/gh-pages/_layouts/default.html).

Just click that link to edit the layout right in your browser.

### Bug in this page?

To fix a bug in this page [click this edit link]({{ site.github.repository_url}}/edit/gh-pages/index.markdown).
