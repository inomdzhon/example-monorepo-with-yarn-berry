# Example monorepo with `yarn@berry`

## Quick start

```
$ npm i -g yarn
$ yarn install
```

## How to reproduce problem?

### 1️⃣ example

Run from root
```
$ yarn workspace ui pack
```
or
```
$ cd packages/ui
$ yarn pack
```

both exit with
```
➤ YN0036: Calling the "prepack" lifecycle script
➤ YN0036: Prepack script failed; run "yarn prepack" to investigate
➤ YN0000: Failed with errors in 1.03s
```

because
```
$ cd packages/ui
$ yarn build
command not found: tsc
```

✅ but if we run command from root
```
$ yarn run packages:ui:build
```
resolve `tsc`.


### 2️⃣ example

✅
```
$ yarn run packages:ui:ci:eslint
```

❌
```
$ yarn workspace ui ci:eslint
command not found: eslint
```
or
```
$ cd packages/ui
$ yarn ci:eslint
command not found: eslint
```

## What is expected?

`tsc` and `eslint` should resolve from root `node_modules`.

`yarn@1.22.4` can resolve this ([go to folder](../yarn-classic)).