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
    <img src="{{ contributor.avatar_url }}" width="32" height="32" />
    <a href="{{ contributor.html_url }}">{{ contributor.login }}</a>
  </li>
{% endfor %}
</ul>

The code for generating that list is:

```
{% raw %}
<ul>
{% for contributor in site.github.contributors %}
  <li>
    <img src="{{ contributor.avatar_url }}" width="32" height="32" />
    <a href="{{ contributor.html_url }}">{{ contributor.login }}</a>
  </li>
{% endfor %}
</ul>
{% endraw %}
```

## Repositories

This is a list of my public repositories

<ul>
  {% for repository in site.github.public_repositories %}
    <li><a href="{{ repository.html_url }}">{{ repository.full_name }}</a></li>
  {% endfor %}
</ul>

```
{% raw %}
<ul>
  {% for repository in site.github.public_repositories %}
    <li><a href="{{ repository.html_url }}">{{ repository.full_name }}</a></li>
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

## Theme

GitHub Pages now support specifying themes outside of your repository. For example, you can use one of GitHub's pre-built themes by entering the following in [`_config.yml`](https://github.com/Haacked/gh-pages-demo/blob/gh-pages/_config.yml)

```
theme: minima
```

GitHub Pages also supports specifying another repository as the theme for your site. See the [documentation for more information](https://help.github.com/articles/adding-a-jekyll-theme-to-your-github-pages-site/).

### Bug in this page?

To fix a bug in this page [click this edit link]({{ site.github.repository_url}}/edit/gh-pages/index.markdown).
