# Baag API docs

Mintlify docs for the Baag API (`https://api.baag.cc/v1`). Pages are MDX with YAML frontmatter; settings and the sidebar live in `docs.json`.

## How it's built

- Endpoint pages (`store`, `products/`, `collections/`, `checkout/`) follow the Taag docs layout: a short, friendly intro ("You can use this endpoint to…"), a `method:` block with the URL, Authorization, Parameters / Request Body (`ParamField`), Response (JSON), then Error Responses as an `AccordionGroup` titled by error name ("Invalid request"). Each page lists all its own errors, key errors included; there's no separate errors page. The `openapi: 'METHOD /path'` frontmatter (path without `/v1`) only gives the sidebar its method badge.
- No playground and no side code samples. Don't add an OpenAPI file: Mintlify would pick it up and bring them back.
- Guides (`introduction`, `authentication`) are plain MDX. The introduction explains in words, with no endpoint list.
- There's one API key (`pk_live_…`) for every endpoint. `sk_live_` keys are rejected.
- The API's code in `Baag-api/src` is the source of truth. Check the routes before documenting a behavior.

## Style

- Simple words, short sentences, second person ("you"). Readers may not be technical: explain what each field means.
- Sentence case for headings.
- Bold for UI elements: **Baag App** → **Settings** → **Developers**.
- Icons only in the sidebar (guide frontmatter), not in page bodies.
- Use `<Note>` and `<Warning>` sparingly, for things a reader must not miss.
- Prices are whole RWF.
