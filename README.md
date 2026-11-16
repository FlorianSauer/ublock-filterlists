# ublock-filterlists

Custom filter lists for uBlock Origin.

## Subscribe

Both host lists in one file; this is the URL to paste into uBO:

```
https://raw.githubusercontent.com/FlorianSauer/ublock-filterlists/main/ublock-filterlists.txt
```

One file per host:

```
https://raw.githubusercontent.com/FlorianSauer/ublock-filterlists/main/heise-de.txt
https://raw.githubusercontent.com/FlorianSauer/ublock-filterlists/main/tumblr-com.txt
```

uBO dashboard -> Filter lists -> "Import…" -> paste a URL.

## Updating

uBO re-fetches every 2 days (`! Expires: 2 days`). 
"Update now" in the dashboard fetches immediately. 
A push to `main` rebuilds the combined file automatically. There is no build step to run.

## Files

| File | Covers |
|---|---|
| `heise-de.txt` | heise+ paywall teasers, self-promo, affiliate best lists, podcast/video/widget modules, sticky action bar |
| `tumblr-com.txt` | cookie banner (CMP), login nags/dialogs, scroll lock |

`ublock-filterlists.txt` (all of the above, concatenated) is rebuilt by CI on each push and committed into this repository. The same file is attached to the latest release as a plain-text download:

```
https://github.com/FlorianSauer/ublock-filterlists/releases/latest/download/ublock-filterlists.txt
```
