linter-js-standard
=========================
This plugin for [Atom Linter](https://github.com/AtomLinter/Linter) provides an interface for error/warning messages from [blyss](https://github.com/saadq/blyss). It is a fork of [linter-js-standard](https://github.com/ricardofbarros/linter-js-standard).

## Installation
Linter package must be installed in order to use this plugin. If Linter is not installed, please follow the instructions [here](https://github.com/AtomLinter/Linter).

### Plugin installation
```
$ apm install linter-js-blyss
```

## Settings

### checkStyleDevDependencies (default: false)
Check code style in package.json `devDependencies` or `dependencies`. If a valid style is not found it won't lint.

> Note: This will use the nearest package.json.

### honorStyleSettings (default: true)
Honors style settings defined in package.json.

Current style settings supported:
- `ignore`
- `parser`

> Note: This will use the nearest package.json.

### style (default: standard)
Switch between standard and semistandard styles.
If `checkStyleDevDependencies` is true this setting will be **ignored**.

### showEslintRules (default: false)
Enable/disable showing the id of the offended eslint rules.

Example of messages while showEslintRules is:
- **true:** Extra semicolon. (semi)
- **false:** Extra semicolon.

### lintMarkdownFiles (default: false)
Lint markdown fenced code blocks.

### Global Variable Support
To have the linter not warn about undeclared variables when using global variables, honorStyleSettings has to be checked/true and a "globals" section has to be added to package.json:
```
"blyss": {
    "globals": [
      "var1",
      "var2"
    ]
  }
  ```
Also see https://github.com/feross/standard#i-use-a-library-that-pollutes-the-global-namespace-how-do-i-prevent-variable-is-not-defined-errors.

## License
MIT
