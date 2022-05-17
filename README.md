# @brlt/eslint-config

- Reasonable defaults for best-practices in **only one-line of config**
- Single quotes, no semicolons
- Auto fix for formatting (to be used standalone without Prettier)
- TypeScript, Vue, React supported out-of-box (_Svelte and Astro support is coming soon_)
- Supports `json`, `yaml`, `markdown`
- Sorted imports and sorted `package.json` fields
- Trailing Commas

<br>

## Installation

```bash
pnpm add -D eslint @brlt/eslint-config
```

<br><hr><br>

## Add to your scripts in `package.json`

```json [package.json]
{
  "scripts": {
    "lint": "eslint .",
    "lint:fix": "eslint . --fix"
  }
}
```

## Configuration

There's no need to fuss with `.eslintignore` most of the time - the preset takes care of that.

The simplest way to integrate this with a project is to use the `eslintConfig` field in `package.json:

<br>

### `package.json`

```json [package.json]
{
  "eslintConfig": {
    "extends": "@brlt"
  }
}
```

<br>

### `.eslintrc` (json)

```json [.eslintrc]
{
  "extends": "@brlt"
}
```

<br>

### `.eslintrc.js`

```js [.eslintrc.js]
module.exports = {
  "extends": "@brlt"
}
```

<br><hr><br>

### Config VS Code auto fix

Create `.vscode/settings.json` if it doesn't already exist, and make sure you have the `dbaeumer.vscode-eslint` extension installed.

```json [.vscode/settings.json]
{
  "prettier.enable": false,
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  }
}
```

<br><hr><br>

## Other Projects

- [nberlette/dotfiles](https://github.com/nberlette/dotfiles) - Personal dotfiles for Gitpod and macOS
- [nberlette/prettier](https://github.com/nberlette/prettier) - Prettier config (independent from this project)

<br><hr><br>

## License

MIT
