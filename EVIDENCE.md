# Evidence for the filter list

This summary refers to the November 21, 2026 Fluxzy investigation. Exchange IDs are included to make the basis of each rule traceable.

| ID | Rule or decision | Evidence |
| --- | --- | --- |
| E1 | Scope both `go.greentrafsa.com` rules to `advtpe.com`. | The inline ad branch references the destination in exchanges **43, 71, 76, and 80**. Exchange **43** contains pop-under logic with `window.open` and focus manipulation. The ordinary resource rule covers the same destination for ABP's ordinary request types. No request to the ad destination was captured. |
| E2 | Preserve the player and media paths. | Exchange **43** contains `/js/player.ec3b7f.js` and inline code that builds signed media URLs. Player documents **43, 71, 76** and `/get_video` redirects **44–45, 72–73, 77–78** establish the route to `*.tapecontent.net`. The capture ends short of a downstream media response. |
| E3 | Keep third-party scripts in the experimental notes. | Exchanges **43, 71, 76, 80** reference `ij.cobolgammed.com` and a loader for `sg.pilotijuly.com`. Exchanges **43, 71, 80** also reference `is.conermoocher.com`. No payload or playback dependency was established for these hosts. |
| E4 | Keep the statistics endpoint and inline anti-adblock code out of production rules. | Exchanges **81–82** show first-party `/stat/…` POSTs. Exchange **43** ties the route to adblock state and contains detection logic in the player document. Selectively blocking that inline code is outside the capabilities of these network rules. |
| E5 | Leave other investigation candidates unclassified. | No supporting exchange or sampled page reference was found for `imedia-stream.com` or `decormyvase.com`. |

The rule syntax and request matching can be checked without contacting the investigated sites. The original evidence identifies a configured ad destination. Blocking effectiveness and playback with the subscription enabled remain untested.
