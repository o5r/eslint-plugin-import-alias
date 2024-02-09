# Improt Alias ESLint Plugin

this is a fork of [eslint-plugin-import-alias](https://github.com/Limegrass/eslint-plugin-import-alias) with the following changes:

-   allow option for ignoring list of files or barrel files

however, this might be a temporary fork until the original plugin is updated with the same changes.

note that the pre commit lint use this eslint package https://github.com/not-an-aardvark/eslint-plugin-self which can be difficult to found and produce error a bit cryptic.

## Original README

## @limegrass/eslint-plugin-import-alias

Encourage use of defined aliases in TSConfig/JSConfig through ESLint.

### Why

-   Automatic imports by tsserver resolve to relative paths that can be normalized.
-   It's easier to refactor by finding and replacing an absolute module path
    without worrying about crafting the regex for `../` and `./`

### Requirements

-   Node 14+

### Install

```shell
npm install --save-dev @limegrass/eslint-plugin-import-alias eslint
```

This plugin relies on an alias configuration in `tsconfig.json`, `jsconfig.json`,
or a config with the same schema and a path given as `aliasConfigPath` in its rules
settings. See the [rules documentation][docs-import-alias] for more detail.

### Configuration

The following is the most basic configuration.
Check the [rules documentation][docs-import-alias] for further configuration.

```jsonc
// .eslintrc
{
    "plugins": ["@limegrass/import-alias"],
    "rules": {
        "@limegrass/import-alias/import-alias": "error"
    }
}
```

This configuration is also turned on automatically if you extend `eslint:recommended`.

[docs-import-alias]: docs/rules/import-alias.md
