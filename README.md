# Item Helper for OGame

A userscript for **OGame v13** (it still runs on v12): a searchable inventory box on the shop page —
what you own, what is already active on this planet, the different durations of an item grouped
under one button, and a jump to the same item on the next planet. It never activates anything — it
opens the game's own item panel and you press the button.

It is a single, self-contained file: install [`OGItemHelper.user.js`](OGItemHelper.user.js), that is
the whole tool.

> **Status: not yet submitted for toleration.** Any tool that runs inside the OGame page must be
> reviewed and tolerated by the OGame Origin team *before* being published. Until that happens this
> repository stays private and the script is not distributed. See [AGENTS.md](AGENTS.md) §5.

It moved here from [PrOGect](https://github.com/nicolagalassi/PrOGect), a collection of OGame
userscripts; its full history came with it.

## Install

1. Install [Tampermonkey](https://www.tampermonkey.net/).
2. Open [`OGItemHelper.user.js`](OGItemHelper.user.js) and install it.

## Compliance

Built against the rules in [AGENTS.md](AGENTS.md) — the OGame Origin team's constraints for
third-party tools. The load-bearing ones for this script:

- **1 click = 1 game action.** It finds and opens the item; activating it stays your click on the
  game's own button.
- **No auto-refresh and no polling.** The account scan is a single read you trigger with a click,
  never a background loop; every interval in the code is a local UI timer that never talks to the
  server.
- **No `cp=` in background calls** — the next-planet jump is a normal navigation you click.
- **No automatically registered alarms.** Nothing watches the game and notifies you.
- **Monetization and legal content untouched** — the Shop and its premium content are never hidden,
  moved, resized or covered.
- **No fees, paywalls or injected ads.** Nothing leaves your machine.

[API-NOTES.md](API-NOTES.md) documents which OGame endpoints are usable and the compliance
constraint attached to each one.

Licensed under the [MIT License](LICENSE).
