# ublock-filterlists

Custom filter lists for uBlock Origin. Rules are built around stable
anchors (`data-*` attributes, `href` paths, ARIA roles, asset file
names) — no generated class names, no prose text anchors on multi-lingual
sites.

## Layout

One list per host, named `<host>.txt`, at the repository root. The set
of hosts grows over time; adding a host means adding one file.

Current lists:

| File | Covers |
|---|---|
| `heise-de.txt` | heise+ paywall teasers, self-promo, affiliate best lists, podcast/video/widget modules, sticky action bar |
| `tumblr-com.txt` | cookie banner (CMP), login nags/dialogs, scroll lock |

## Subscribing (uBlock Origin)

1. uBO dashboard → Filter lists → "Import…" at the bottom
2. Paste the raw URL of a list:

```
https://raw.githubusercontent.com/FlorianSauer/ublock-filterlists/main/heise-de.txt
https://raw.githubusercontent.com/FlorianSauer/ublock-filterlists/main/tumblr-com.txt
```

## Updating

```
git add -A
git commit -m "<host>: <what changed and why>"
git push
```

The push is the release. uBO re-fetches on its own schedule
(`! Expires: 2 days` in each header); force an immediate check via
dashboard → Filter lists → "Update now".

## Adding a new host

1. Facts first: measure the live page, dump the markup, find the
   structural hooks before writing a single rule.
2. Create `<host>.txt` with the standard header (`Title`,
   `Description`, `Homepage`, `Expires`, `Version`, `Last modified`,
   `Licence`).
3. Anchor preference order: `data-*` attribute → `href` path / asset
   file name → ARIA → DOM structure → text anchor (monolingual sites
   only).
4. Every rule carries a comment: what it hides, which anchor it uses,
   why. Record the measured hit count where useful.
5. Commit per host.

## Conventions

- No hashed/generated class names, no prose `:has-text()` anchors on
  multi-lingual sites.
- Every rule is measured against the live page before inclusion;
  unmeasured rules do not ship.
