# NoScript Crowdsourced Whitelist & Blocklist

A community-maintained domain database for [NoScript](https://noscript.net/) — the popular Firefox extension that blocks JavaScript, Flash, and other executable content.

## What's Included

| File | Description | Domains |
|------|-------------|---------|
| `noscript_data.json` | **Ready-to-import** NoScript config file | 846 trusted, 13,284 blocked |
| `capability.policy.maonoscript.sites` | Legacy whitelist (for `about:config`) | — |
| `noscript.untrusted` | Legacy blocklist (for `about:config`) | — |

### Blocklist Sources

The blocklist includes domains from:

- Original crowdsourced submissions
- [Peter Lowe's ad server list](https://pgl.yoyo.org/adservers/) — a well-maintained blocklist of ad/tracking domains

## Usage

### Method 1: Import JSON (Recommended)

1. Download [`noscript_data.json`](./noscript_data.json)
2. Open NoScript settings → Click the gear icon
3. Go to **Export/Import** → **Import**
4. Select the downloaded file

> ⚠️ **Warning**: This will overwrite your existing NoScript configuration. Export your current settings first if you want to merge manually.

### Method 2: Manual Configuration (Legacy)

For older NoScript versions or manual control:

1. Navigate to `about:config` in Firefox
2. Search for `capability.policy.maonoscript.sites` (whitelist) or `noscript.untrusted` (blocklist)
3. Right-click → **Modify** to edit values

## Contributing

Want to add or remove domains? Please ensure:

- **For whitelist additions**: The domain has no bad reputation and isn't flagged by [Google Safe Browsing](https://transparencyreport.google.com/safe-browsing/search)
- **For blocklist additions**: The domain is a known ad server, tracker, or malicious site (ideally already listed in a reputable blocklist like EasyList or StevenBlack)
- The domain isn't compromised by XSS or other attacks
- WHOIS information is valid and the site owner is identifiable

## Why Use This?

**Pros:**

- Block ads, trackers, and malicious scripts by default
- Curated whitelist lets legitimate sites work without manual intervention
- More privacy than browser defaults

**Cons:**

- If you never visit a whitelisted site, those entries are unnecessary (but harmless)
- Some sites may still break if they use unlisted CDNs or third-party scripts

## Links

- [NoScript Official Site](https://noscript.net/)
- [NoScript Firefox Add-on](https://addons.mozilla.org/en-US/firefox/addon/noscript/)
- [NoScript Forums](https://forums.informaction.com/viewforum.php?f=3)

## License

Apache License v2.0 — See [LICENSE](./LICENSE)

---

*Originally created by [CHEF-KOCH](https://github.com/CHEF-KOCH).*
