# Example monorepo with `yarn@1.22.4`

## Quick start

```
$ npm i -g yarn
$ yarn install
```

## No problems.

### 1️⃣ example

✅
```
$ yarn workspace ui pack
```

✅
```
$ cd packages/ui
$ yarn build
```

✅
```
$ cd packages/ui
$ yarn pack
```

### 2️⃣ example

✅
```
$ yarn run packages:ui:ci:eslint
```

✅
```
$ yarn workspace ui ci:eslint
```

✅
```
$ cd packages/ui
$ yarn ci:eslint
command not found: eslint
```
