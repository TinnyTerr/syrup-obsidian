# Syrup on Obsidian

This plugin provides syntax highlighting and execution of the `syrup` and `ask` languages.
Specifically for the CS103 and CS106 classes at Strathclyde University.

| Language | Syntax highlighting            | Execution                        | Hidden Code                                                             |
| -------- | ------------------------------ | -------------------------------- | ----------------------------------------------------------------------- |
| Syrup    | Supported fully, using `syrup` | Supported, using `syrup-compute` | Supported, using `syrup-compute-add` or the inverse `syrup-add-compute` |
| Ask      | Supported, using `ask`         | Unsupported at this time         | Also unsupported at this time                                           |

## Install

1. Download `main.js`, `manifest.json` and `styles.css` from the [latest release](https://github.com/TinnyTerr/syrup-obsidian/releases/latest).
2. Put them in `<your vault>/.obsidian/plugins/syrup/` (create the folder if it isn't there).
3. In Obsidian, go to **Settings → Community plugins**, turn off Restricted mode if it's on, and enable **Syrup**.

To check a release came from this repo's build, run `gh attestation verify main.js --repo TinnyTerr/syrup-obsidian`.

## Use

Fence a block with one of these languages:

````markdown
```syrup
-- highlighted only
```

```syrup-compute
-- highlighted, and the output is shown below
```

```syrup-add
-- highlighted, and fed to the note's shared file, no output
```

```syrup-compute-add
-- as syrup-compute, and fed to the shared file
```

```ask
-- highlighted only
```
````

Blocks in a note run in order and share one file, so a `syrup-compute` block can use anything defined in the `-add` blocks above it. Wrap a block in `%% ... %%` to hide it while still feeding the shared file.


### Syrup

Currently, the js implementation of syrup found [here](https://github.com/TinnyTerr/syrup-ts) is compiled in the release step of this plugin, and its source cannot be found here.
However, its development, however faithful to the language, is still incomplete, and therefore any results from its response to code should be at least taken with a grain of salt.

### Ask

Ask has no js implementation, and it will be worked on once syrup is complete. This also means I have no timeline for when this will be complete, and will be added in due course.
