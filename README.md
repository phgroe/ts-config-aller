# TypeScript Config Aller

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](http://www.gnu.org/licenses/mit)
&nbsp;
[![NPM version](https://img.shields.io/npm/v/@aller/ts-config-aller.svg)](https://www.npmjs.com/package/@aller/ts-config-aller)

Aller Media's common configuration files for TypeScript projects. These include:

* **tsconfig.json** -- the Compiler
* **tslint.js** -- the Linter

## Installation

Get started by running this command in the root of your project:

```sh
npm install --save-dev @aller/ts-config-aller
cp node_modules/@aller/tsconfig.example.json tsconfig.json
cp node_modules/@aller/tslint.example.json tslint.json
```

## Setup

### TypeScript Compiler

The `tsc` compiler expects a configuration file in the root directory of the project:

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

The sections `files` and `include` determine which files or locations will be picked up by the compiler. Please refer to [the official documentation](http://www.typescriptlang.org/docs/handbook/tsconfig-json.html#examples) for detailed examples.

### TSlint

The configuration for _TSlint_ was originally taken from [Reader Critics](https://github.com/dbmedialab/reader-critics) and then extended/modified with some of the rules that already have an equivalent in the _ESlint_ configurations which are used in our department:

```json
{
	"extends": "@aller/ts-config-aller"
}
```

Most of the rules are actually equal to those of [Airbnb](https://github.com/progre/tslint-config-airbnb) with the exception of a few which we found annoying. Additionally, we don't use custom rulesets.

## License

**Copyright © 2017 DB Medialab / Aller Media AS** (Oslo, Norway)

Licensed under the [MIT License](LICENSE.txt).
