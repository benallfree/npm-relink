# NPM Relink

This package re-establishes symlinks after `npm i` has run. This shortcoming of npm is a [known issue](https://github.com/npm/npm/issues/17287) that the npm team has been slow to fix, so here is a package to do it.

## Installation

```bash
% npm install -g npm-relink
```

## Usage

Initialize from your project root:

```bash
% npm-relink init
% echo ".npm-relink.json" >> .gitignore
```

Any time you run `npm install`, run `npm-relink` afterward.

When you run `npm link', run 'npm-relink init` afterward to capture changes.

## Further Development

I wish there were a way to do a post hook for dependency installation via `npm install <package>`. Something like `depinstall` [ticket opened here](https://github.com/npm/cli/issues/962)
