# ublock-filterlists

Custom filter lists for uBlock Origin.

## Subscribe

Every host list in one file:

```
https://github.com/FlorianSauer/ublock-filterlists/releases/latest/download/ublock-filterlists.txt
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

`ublock-filterlists.txt` (all of the above, concatenated) is built by the release workflow. 
It is not stored in this repository.
