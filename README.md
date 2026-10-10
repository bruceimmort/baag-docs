# Baag API docs

The documentation for the Baag API (`api.baag.cc`), built with [Mintlify](https://mintlify.com).

## Run it locally

```bash
npm i -g mint
mint dev          # http://localhost:3000
```

Run it from this folder, where `docs.json` is.

## Where things are

| | |
|---|---|
| `docs.json` | Site settings and the sidebar |
| `*.mdx` | The "Get started" guides |
| `v1/` | One page per endpoint, written by hand like the Taag docs |

## Before you push

```bash
mint broken-links
```

When the API changes, update its endpoint page. The API's code (`Baag-api/src/routes`) is the source of truth.
