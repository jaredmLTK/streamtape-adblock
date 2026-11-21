# Streamtape AdBlock

An Adblock Plus-format subscription for the Streamtape-associated player observed at `advtpe.com`. It targets one configured advertising destination, `go.greentrafsa.com`.

## Subscribe

- [GitHub Pages subscription](https://jaredmltk.github.io/streamtape-adblock/streamtape.txt)
- [GitHub Raw subscription](https://raw.githubusercontent.com/jaredmLTK/streamtape-adblock/main/streamtape.txt)

Aloha's iOS release notes list URL-based custom subscriptions starting in version **8.6.0**. In Aloha, open **Settings → AdBlock**, look for **Custom Filter Lists** under **Filter Lists**, and add one of the URLs above. Aloha documents URL import for iOS. The exact menu nesting may vary by release. [Aloha's iOS release notes](https://apps.apple.com/us/app/aloha-browser-private-vpn/id1105317682)

## What the list matches

- The `$popup` rule matches the configured destination in a new window or tab opened from the observed player, where the client implements that modifier.
- The ordinary network rule matches requests to the same destination initiated by the player, where the client supports domain-scoped network filtering. In Adblock Plus it applies to ordinary resource types such as scripts and frames. Popups and top-level navigation use different request types.

The list can block a matching destination load while page JavaScript can still attempt to open or switch tabs. Aloha's handling of these individual modifiers and playback with the list enabled remain unverified. Aloha also has built-in **Block pop-ups** and **Block app redirects** controls. [Adblock Plus syntax](https://help.adblockplus.org/adblock-plus-help-center/how-to-write-filters) · [Aloha's AdBlock controls](https://community.alohabrowser.com/knowledge-base/article/how-can-i-enable-adblock_1)

## Updates

Keep `streamtape.txt` at the root of `main` so existing subscription URLs stay valid. When changing active rules, increment the numeric list version, update the modification date and [changelog](CHANGELOG.md), and document the technical justification in [Evidence](EVIDENCE.md). Run parser and matching checks on the new rule and protected player paths before publication. Client refresh timing can vary. The list advertises a seven-day refresh interval.

[Experimental notes](experimental.txt) contain commented-out candidates. Subscribe to `streamtape.txt` for the production list.
