---
title: Getting started
sidebar_label: Getting started
---

# Getting started

**Boxed** provides essential building-blocks (in the form of types and functions) so that you can write functional, safe TypeScript code.

```ts
const make = (input) =>
  Option.fromNullable(input)
    .map(parseInput)
    .flatMap((input) => Option.fromNullable(transform(input)))
    .map(print)
    .map(prettify)
    .getOr("fallback");
```

## Design principles

- Provide utility types that **make data-manipulation and storage easier**
- **Immutable** (all provided types are)
- Give a **good development experience** (chaining API, reliable types)
- Simple **interoperability** (you can convert back and forth to JS native types)
- Compatibility with `ts-pattern` (using `patterns` we provide).

## What's in the box?

- `Option<Value>`
- `Result<Ok, Error>`
- `AsyncData<Value>`
- `Future<Value>`
- `Lazy<Value>`
- Some utils like `Deferred`, `Dict` & `Array`

## Install

```console
$ yarn add @swan-io/boxed
```

or

```console
$ npm install @swan-io/boxed
```

## Inspirations

- [ReScript's Belt Stdlib](https://rescript-lang.org/docs/manual/latest/api/belt)
- [ReScript Future](https://github.com/bloodyowl/rescript-future)
- [ReScript AsyncData](https://github.com/bloodyowl/rescript-asyncdata)
