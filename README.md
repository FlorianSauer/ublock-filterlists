# ublock-filterlists

Custom filter lists for uBlock Origin.

## Subscribe

Both host lists in one file; this is the URL to paste into uBO:

```
https://floriansauer.github.io/ublock-filterlists/ublock-filterlists.txt
```

One file per host:

```
https://raw.githubusercontent.com/FlorianSauer/ublock-filterlists/main/domain-lists/heise-de.txt
https://raw.githubusercontent.com/FlorianSauer/ublock-filterlists/main/domain-lists/tumblr-com.txt
https://raw.githubusercontent.com/FlorianSauer/ublock-filterlists/main/domain-lists/discord-com.txt
```

uBO dashboard -> Filter lists -> "Import…" -> paste a URL.

## Updating

uBO re-fetches every 2 days (`! Expires: 2 days`). 
"Update now" in the dashboard fetches immediately. 
A push to `main` goes live at the next fetch.

## Files

| File | Covers |
|---|---|
| `domain-lists/heise-de.txt` | heise+ paywall teasers, self-promo, affiliate best lists, podcast/video/widget modules, sticky action bar |
| `domain-lists/tumblr-com.txt` | cookie banner (CMP), login nags/dialogs, scroll lock |
| `domain-lists/discord-com.txt` | terms consent popup in the web client (image viewer, soundboard and settings dialogs stay) |

`ublock-filterlists.txt` (all of the above in one) is built automatically and served at the subscription URL above. The same file is attached to the latest release as a plain-text download:

```
https://github.com/FlorianSauer/ublock-filterlists/releases/latest/download/ublock-filterlists.txt
```
