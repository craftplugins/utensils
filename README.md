# Craft Utensils

A plugin for [Craft](http://craftcms.com) that extends the functionality of [Twig](http://twig.sensiolabs.org/).

The goal of this project is to deliver helpful templating functionality in a single plugin.

```jinja
{% unless currentUser.admin %}
  {% redirect 'login' %}
{% endunless %}

There’s {{ entries|length }} {{ 'entry' | pluralize(entries|length) }}!

<div class="bg-img-{{ asset.id | md5 }}"></div>

{{ gist(bb45340bc4eda4c7d932, 'general.php') }}

{{ craft.request.segment(4) | humanize }}
```

## Installation

1. Copy the `utensils/` folder into `craft/plugins/`
2. Go to Settings → Plugins and click the “Install” button next to “Utensils”

## Usage

There’s far too much to document on a single page. Have a look at the [Functions](docs/functions.md), [Filters](docs/filters.md), and [Tags](docs/tags.md) documentation for more.

### Functions
- [lipsum](docs/functions.md#lipsum-paragraphs5-htmltrue-min20-max100-)
- [gist](docs/functions.md#gist-id-filenull-)
- [pastebin](docs/functions.md#pastebin)

### Filters
- General
  - [center](docs/filters.md#center-width80-)
  - [md5](docs/filters.md#md5)
  - [sha1](docs/filters.md#sha1)
  - [sha512](docs/filters.md#sha512)
- Inflection
  - [pluralize](docs/filters.md#pluralize-num2-)
  - [singularize](docs/filters.md#singularize)
  - [camelize](docs/filters.md#camelize)
  - [dasherize](docs/filters.md#dasherize)
  - [humanize](docs/filters.md#humanize)
  - [hyphenate](docs/filters.md#hyphenate)
  - [ordinalize](docs/filters.md#ordinalize)
  - [pascalize](docs/filters.md#pascalize)
  - [titleize](docs/filters.md#titleize)
  - [underscore](docs/filters.md#underscore)

### Tags
- [unless](docs/tags.md#unless)
- [less](docs/tags.md#less)
