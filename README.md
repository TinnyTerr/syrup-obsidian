# Syrup on Obsidian

This plugin provides syntax highlighting and execution of the `syrup` and `ask` languages.
Specifically for the CS103 and CS106 classes at Strathclyde University.

| Language | Syntax highlighting            | Execution                        | Hidden Code                                                             |
| -------- | ------------------------------ | -------------------------------- | ----------------------------------------------------------------------- |
| Syrup    | Supported fully, using `syrup` | Supported, using `syrup-compute` | Supported, using `syrup-compute-add` or the inverse `syrup-add-compute` |
| Ask      | Supported, using `ask`         | Unsupported at this time         | Also unsupported at this time                                           |

## Use

### Syrup

Currently, the js implementation of syrup found [here](https://github.com/TinnyTerr/syrup-ts) is compiled in the release step of this plugin, and its source cannot be found here.
However, its development, however faithful to the language, is still incomplete, and therefore any results from its response to code should be at least taken with a grain of salt.

### Ask

Ask has no js implementation, and it will be worked on once syrup is complete. This also means I have no timeline for when this will be complete, and will be added in due course.
