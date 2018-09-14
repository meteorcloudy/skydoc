---
layout: default
title: Writing Documentation
---

## Rule Documentation

When generating documentation, Stardoc parses the `.bzl` file to extract the
inline documentation as well as evaluates the Starlark code to determine the
types for rule attributes.

Private rule attributes (i.e. those whose names begin with `_`) will not
appear in generated documentation.

[Starlark Rules](https://bazel.build/docs/skylark/rules.html) are declared using
the `rule()` function as global variables.

General rule documentation should be supplied in the `doc` parameter of the
`rule()` function.

Likewise, supply attribute documentation in the `doc` parameter of attribute
schema-defining functions, such as `attr.label()`.

```python
my_rule = rule(
    implementation = _my_rule_impl,
    doc = """
Example rule documentation.

Example:
  Here is an example of how to use this rule.
""",
    attrs = {
        "srcs" : attr.label_list(
            doc = "Source files used to build this target.",
        ),
        "deps" : attr.label_list(
            doc = "Dependencies for this target.",
        ),
    }
)
```

The `name` attribute that is common to all rules is documented by default.

