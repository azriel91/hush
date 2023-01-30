+++
title = "hush"
template = "home.html"
insert_anchor_links = "heading"
sort_by = "weight"
+++

**hush** is a gentle and responsive Zola theme for product sites, forked from [Juice](https://juice.huhu.io/).

* Designed for product sites
* Responsive and mobile device compatible


# Installation

First download this theme to your `themes` directory:

```bash
$ cd themes
$ git clone https://github.com/azriel91/hush.git
```

or add as a submodule:

```bash
$ git submodule add https://github.com/azriel91/hush themes/hush
```

and then enable it in your `config.toml`:

```toml
theme = "hush"
```


## Structure

### Hero

**hush** is designed for product websites, hence we let **hero** part fills whole of screen.
You can customize your **hero** by using `hero` block in the `index.html`.

```html
{% extends "hush/templates/index.html" %}
{% block hero %}
    <div>
        Your cool hero html...
    </div>
{% endblock hero %}
```

### Page

Every markdown file located in `content` directory will become a **Page**. There also will display as
a navigate link on the top-right corner.
You can change the frontmatter's `weight` value to sort the order (ascending order).

```
+++
title = "Changelog"
description = "Changelog"
weight = 2
+++

```


### CSS variables

You can override theme variable by creating a file named `_variables.html` in your `templates` directory.

See the default value [here](./templates/_variables.html)


### Favicon

```html
{% extends "hush/templates/index.html" %}
{% block favicon %}
    <link rel="icon" type="image/png" href="/favicon.ico">
{% endblock favicon %}
```


## Configuration

You can customize some builtin property in `config.toml` file:

```toml
[extra]
hush_logo_name = "hush"
hush_logo_path = "dove.svg"
hush_extra_menu = [
    { title = "Github", link = "https://github.com/azriel91/hush"}
]
hush_exclude_menu = [
    "exclude_from_nav"
]
repository_url = "https://github.com/azriel91/hush"
```


# Shortcodes

**hush** have some builtin shortcodes available in `templates/shortcodes` directory.

* `issue(id)` - A shortcode to render issue url, e.g. `issue(id=1)` would render to the link `https://github.com/azriel91/hush/issue/1`.

> The `repository_url` is required.


# Contributing

Thank you very much for considering contributing to this project!

We appreciate any form of contribution:

* New issues (feature requests, bug reports, questions, ideas, ...)
* Pull requests (documentation improvements, code improvements, new features, ...)
