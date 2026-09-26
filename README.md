# nib-plugins

The list of plugins for [nib](https://github.com/nib-editor/nib) that you can find and install by name:

```sh
nib plugin search status
nib plugin add wordcount
```

The name is only a shortcut: nib installs from the plugin's `source` and remembers that, the same as `nib plugin add owner/repo`. Being listed here says nothing about what a plugin does; nib shows the capabilities a plugin asks for and asks before installing it.

## Adding a plugin

Open a pull request that adds an entry to [plugins.toml](plugins.toml), in order by name:

```toml
[[plugin]]
name = "wordcount"                     # the name in the plugin's plugin.toml
source = "nib-editor/plugin-example"   # anything `nib plugin add` takes
description = "What it does, in one line"
```

- `name` must be the plugin's own name, and not taken by another entry or by a plugin built into nib.
- `source` is usually a GitHub repository whose releases have one `*.nib.tar.gz`, made with `nib plugin pack`. See [nib-plugin-example](https://github.com/nib-editor/plugin-example) for a repository that builds and releases one.

A check makes sure the file parses and the names are unique and in order.

## License

The list is available under [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).
