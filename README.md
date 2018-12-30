# pos-utils

Utility module for PlatfromOS

# Installation

Place all the files in the modules/ directory

# Usage

There are two ways of using prefefined components of utils library:

## Direct

At anytime you can use direct partial path to include predefined component:

``` 
  {% include "modules/utils/utils/inputs/submit_tag" with "Log Out", class: "btn btn-info ml-auto mr-5" %}
```

## With predefined variable

1. Include `modules/utils/inti` partial and parsie it with `parse_json` tag: 

```
{% parse_json "utils" %}
  {%- include 'modules/utils/init' -%}
{% endparse_json %}
```

2. Use predefined components paths with `utils` variable:

```
  {% include utils.flash_messages %}
  {% include utils.input with form_builder.fields.email, type: "text" %}
```



# Configuration

Utils module provide some global configuration options, you can instpect all of possible configuration option by simply displaying global object:

```
{{ context.exports.utils.config }}

```

It is possible to manipulate those configuration options by simply defining them while including init file:

```  
{% parse_json "utils" %}
  {%- include 'modules/utils/init', default_wrapper_class: "some-new-class" -%}
{% endparse_json %}
```

# development

`git submodule add https://github.com/appko/pos-utils.git modules/utils`
