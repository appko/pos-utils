# pos-utils

Utility module for PlatfromOS

# installation

place all the files in the modules/ directory

create configuration file in marketplace_builder/views/partials/config/\_utils.liquid

```code
{% parse_json _utils_config %}
  {
    "default_wrapper_class": "form-group mb-3",
    "default_input_class": "form-control"
  }
{% endparse_json %}
```

# development

`git submodule add https://github.com/appko/pos-utils.git modules/utils`
