# Baag API docs

Mintlify docs for the Baag API (`https://api.baag.cc/v1`). Pages are MDX with YAML frontmatter; settings and the sidebar live in `docs.json`.

## How it's built

- Endpoint pages in `v1/` follow the Taag docs layout: one-line intro, a `method:` block with the URL, Authorization, Parameters / Request Body (`ParamField`), Response (JSON), then Error Responses as an `AccordionGroup` titled by error name ("Invalid request"). The `openapi: 'METHOD /path'` frontmatter only gives the sidebar its method badge.
- No playground and no side code samples. Don't add an OpenAPI file: Mintlify would pick it up and bring them back.
- Guides (`introduction`, `authentication`, `checkout`, `pagination`, `errors`) are plain MDX.
- The API's code in `Baag-api/src` is the source of truth. Check the routes before documenting a behavior.

## Style

- Simple words, short sentences, second person ("you").
- Sentence case for headings.
- Bold for UI elements: **Baag App** → **Settings** → **Developers**.
- Icons only in the sidebar (guide frontmatter), not in page bodies.
- Use `<Note>` and `<Warning>` sparingly, for things a reader must not miss.
- Prices are whole RWF.
