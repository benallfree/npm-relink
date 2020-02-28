# NPM Relink

This package re-establishes symlinks after `npm i` has run. This shortcoming of npm is a [known issue](https://github.com/npm/npm/issues/17287) that the npm team has been slow to fix, so here is a package to do it.

## Installation

```bash
% npm install -g npm-relink
```

## Usage

In your `package.json`:

```json
"scripts": {
    "postinstall": "npm-relink"
}
```

Initialize from your project root:

```bash
% npm-relink init
% echo ".npm-relink.json" >> .gitignore
```

Any time you run `npm link`, run `npm-relink init` afterward, or just add the package name to `.npm-relink.json` directly.
