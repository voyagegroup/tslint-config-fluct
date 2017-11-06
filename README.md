# tslint-config-fluct

[![Build Status](https://travis-ci.org/voyagegroup/tslint-config-fluct.svg?branch=master)](https://travis-ci.org/voyagegroup/tslint-config-fluct)


## Basic Principles for Settings

- _Fill the rest of space which are not covered by TypeScript compiler_.
    - So we recommends to use this as warning.
- Ban a dangerous style.
- Sort a style to avoid errors and to increase productivity.


## How To Use

### 1. install to your project

- As npm package (TBD. see [#5](https://github.com/voyagegroup/tslint-config-fluct/issues/5))
- Specify tar.gz to a dependency field in your package.json.
    - `"tslint-config-fluct": "https://github.com/voyagegroup/tslint-config-fluct/archive/<COMMIT_HASH>.tar.gz"`.
    - Please replace `<COMMIT_HASH>` with tag name (e.g. `v1.2.3`), or an arbitary commit hash.
        - You can specify `master` or other branch directly. But we don't recommend it strongly.


### 2. Set up your `tslint.json`

```javascript
{
    "extends": [
        "./node_modules/tslint-config-fluct/config/basic.json", // builtin basic rules.
        "./node_modules/tslint-config-fluct/config/typecheck.json" // builtin typecheck rules.
    ],

    "defaultSeverity": "warning",

    "rules": {
    }
}
```

1. Import via `extends` fields in your `tslint.json`
2. Set `defaultSeverity`.
3. Enable/Disable more rules via `rules` by the requirement for your project.

see also: [TSLint's document](https://palantir.github.io/tslint/usage/configuration/)


## License

- [The MIT License](./LICENSE.txt)
    - Original: https://opensource.org/licenses/MIT


## Dependencies

- [yarn](https://yarnpkg.com/)
    - We uses the latest now.
