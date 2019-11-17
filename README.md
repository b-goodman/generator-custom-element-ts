# generator-custom-element-ts

Start a new custom element using Typescript, extending `HTMLElement`.

+ Define a Typescript class extending HTMLElement.
+ Optionally import scss styles or inline within HTML template.
+ es module build.
+ Basic dev server (no live reload)

## Install

[Yeoman](https://yeoman.io/) is a pre-requisite so make sure its installed first.

```bash
npm i -g yo
```

Install the generator

```bash
npm i -g generator-custom-element-ts
```

## Usage

```bash
$ yo custom-element-ts

# This will set the element's tag name and the name of the project's root directory.
? Name of element: new-element

? Select package manager (Use arrow keys)
❯ npm
  yarn
```

Name is verified using [validate-element-name](https://www.npmjs.com/package/validate-element-name)

```bash
? Name of element: New-Element
>> Custom element names must not contain uppercase ASCII characters.

? Name of element: new
>> Custom element names must contain a hyphen. Example: unicorn-cake
```

## What You Get

### Template

```text
.
├── README.md
├── index.html
├── package.json
├── rollup.config.js
├── src
│   ├── index.ts
│   ├── index.scss
│   └── scss.d.ts
└── tsconfig.json
```

### Scripts

Run `name` with either `npm run` or `yarn`.

| name    | command                                           |
|---------|---------------------------------------------------|
|`build`  | `./node_modules/.bin/rollup -c ./rollup.config.js`|
|`start` | `./node_modules/.bin/serve`                       |
