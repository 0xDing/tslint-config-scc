# tslint-config-scc

Code style checking for Sequoia Capital China Typescript repositories. Forked from [shopify/tslint-config-shopify](https://github.com/Shopify/tslint-config-shopify).

## Installation

Install [TSlint](https://palantir.github.io/tslint/) and `tslint-config-scc`:

```
yarn add --dev tslint tslint-config-shopify
```


## Usage
SCC’s TSLint rules come bundled in `tslint-config-scc`.
To enable these rules, create a `tslint.json` file at the root level of your project, and extend `tslint-config-scc`.
```
{
  "extends": "tslint-config-scc"
}
```

Now you can run TSLint by adding the following linting script to your `package.json`. See [here](https://palantir.github.io/tslint/usage/cli/) for more script configurations.
```
{
  "scripts": {
    "lint": "tslint './src/**/*.{ts,tsx}' --project tsconfig.json"
  }
}
```
Run it:

```
yarn run tslint
```

## Configuration

* See [here](https://palantir.github.io/tslint/usage/tslint-json/) for more details on configuring your `tslint.json`.
* See [here](https://palantir.github.io/tslint/rules/) for all the rules provided by [TSlint](https://palantir.github.io/tslint/)

Some of the rules configured in `tslint-config-scc`  may not be sufficient for your project. You can override these rules in `tslint.json`:

```json
{
  "extends": "tslint-config-scc",
  "rules": {
    "no-console": false
  }
}
```

> (c) 2018 Sequoia Capital.
