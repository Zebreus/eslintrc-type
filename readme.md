# Eslintrc Type

A `.eslintrc.json` type, regularly regenerated based on [the schemastore.org definition](https://json.schemastore.org/eslintrc.json).

## Installation

```sh
npm i eslintrc-type
```

## Usage

```ts
import {Eslintrc} from "eslintrc-type";

const eslintrc: Eslintrc = {
    // ...
};
```

## Rationale

I want to generate eslint config files from javascript objects. For that I want to have the correct type. This is a fork from [`tsconfig-type`](https://github.com/harrysolovay/tsconfig-type), the only thing I did was replacing `tsconfig` with `eslintrc`.

`eslintrc-type` is regularly (on a weekly basis) regenerated from the latest JSON schema. First, the generation script fetches the JSON schema and runs it through [`json-schema-to-typescript`](https://github.com/bcherny/json-schema-to-typescript). Next, that output undergoes a series of transforms. Finally, the resulting type is auto-published to NPM with a minor version increment. In this regard, this package does not strictly follow semver (I'd recommend pinning).
