# TypeScript Config Aller

Aller Media's common configuration files for TypeScript projects. This includes:

* tsconfig.json -- the compiler
* tslint.json -- the linter

... prettier ?

## Installation

Get started by running this command in the root of your project:

```sh
yarn add eslint @aller/ts-config-aller --dev
```
or
```sh
npm install --save-dev @aller/ts-config-aller
```

## Setup

### TypeScript Compiler

The `tsc` compiler expects a configuration file in the root directory of the
project. Copy+paste this info a file named `tsconfig.json` in your project root:

```json
{
    "extends": "./node_modules/@aller/ts-config-aller/tsconfig.json",
    "files": [
        ...
    ],
    "include": [
        ...
    ],
    "compilerOptions": {
        "outDir": "dist"
    }
}
```

The sections `files` and `include` determine which files or locations will be
picked up by the compiler and used as source locations. Please refer to
[the official documentation](http://www.typescriptlang.org/docs/handbook/tsconfig-json.html#examples)
for some examples.

### TSlint

