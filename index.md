## Ship Power Plants

<nav id="navbar" class="collapse navbar-collapse">
    <ul class="nav navbar-nav">
        {% assign links = site.data.navigation %}
        {% for link in links %}
            {% assign class = nil %}
            {% if page.url contains link.url %}
                {% assign class = 'active' %}
            {% endif %}
            {% if link.sublinks %}
                <li class="dropdown {{ class }}">
                    <a href="{{ site.baseurl }}{{ link.url }}" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">{{ link.title }} <span class="caret"></span></a>
                    <ul class="dropdown-menu">
                        {% for sublink in link.sublinks %}
                            {% if sublink.title == 'separator' %}
                                <li role="separator" class="divider"></li>
                            {% else %}
                                <li>
                                    <a href="{{ site.baseurl }}{{ sublink.url }}">{{ sublink.title }}</a>
                                </li>
                            {% endif %}
                        {% endfor %}
                    </ul>
                </li>
            {% else %}
             <li class="{{ class }}">
                    <a href="{{ site.baseurl }}{{ link.url }}">{{ link.title }}</a>
                </li>
            {% endif %}
        {% endfor %}
    </ul>
</nav>

You can use the [editor on GitHub](https://github.com/vbily/oma/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/vbily/oma/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
