Chrome Web Store Submission
===========================

Submission record for the Chrome Web Store listing of **Cloud To Butt** (Manifest V3, v2.0).

Status: **Submitted for review** on 2026-06-23.

Listing details
---------------

| Field | Value |
|-------|-------|
| Name | Cloud To Butt |
| Version | 2.0 |
| Manifest | V3 |
| Category | Fun |
| Visibility | Public |
| Package | `cloud-to-butt-v2.0.zip` |
| Icon (128) | `Source/icons/icon128.png` |
| Small tile (440x280) | `store_tile_440x280.png` |
| Screenshot (1280x800) | `screenshot_1280x800.png` |

Summary
-------

> Replaces every mention of 'cloud' with 'butt' — and 'the cloud' with 'my butt'.

Description
-----------

> The classic cloud-to-butt extension, revolutionized for modern Chrome. Built on Manifest V3 and broadened so every mention of "cloud" becomes "butt" — case preserved. "The cloud" becomes "my butt." Cloudflare becomes buttflare. CLOUD becomes BUTT. The future of computing is here.

Single purpose
--------------

> Replaces occurrences of the word "cloud" with "butt" in text on web pages.

Permission justification (`*://*/*`)
-------------------------------------

> The extension replaces the word "cloud" with "butt" in visible text on web pages. To perform this replacement automatically as the user browses, content scripts must run on every page the user visits. A narrower host match would silently skip pages and defeat the single purpose. The extension reads and modifies only text nodes in the page DOM; it does not collect, store, or transmit any data, and makes no network requests.

Privacy practices
-----------------

- **Data collection**: None. The extension does not collect, store, or transmit any user data.
- **Remote code**: None. All code is bundled in the package; no remote scripts are loaded.
- **Data sale / sharing**: N/A — no data is handled.
- **Authentication**: None.
- **WebRTC**: Not used.

Review notes
------------

- This extension requests all-hosts (`*://*/*`) because its single purpose is automatic text replacement on every page the user visits. Narrower matches would silently break the functionality.
- It is a content-script-only extension: no background service worker, no popup, no options page, no network calls.
- The extension is a fork of [panicsteve/cloud-to-butt](https://github.com/panicsteve/cloud-to-butt), modernized to Manifest V3 and broadened to replace every mention of "cloud" (not just the phrase "the cloud"). Upstream PR: [panicsteve/cloud-to-butt#78](https://github.com/panicsteve/cloud-to-butt/pull/78).

Possible review friction
------------------------

1. **Broad text modification** — reviewers sometimes flag extensions that modify all page text. Fallback: narrow back to `the cloud` -> `my butt` only.
2. **Name / "butt" wording** — if flagged as inappropriate, fallback name: "Cloud To Bottom".

Rebuild the package
-------------------

```
cd Source && zip -r ../cloud-to-butt-v2.0.zip manifest.json content_script.js icons/
```

Install (developer / unpacked)
------------------------------

1. Open `chrome://extensions`.
2. Enable **Developer mode**.
3. Click **Load unpacked**.
4. Select the `Source/` folder.
