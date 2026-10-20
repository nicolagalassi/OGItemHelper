# Item Helper for OGame

![Item Helper for OGame](https://i.ibb.co/chPtsm2w/itemhelper.jpg)

A userscript for **OGame v13** (it still runs on v12): a searchable inventory box on the shop page —
what you own, what is already active on this planet, the different durations of an item grouped
under one button, and a jump to the same item on the next planet. It never activates anything — it
opens the game's own item panel and you press the button.

It is a single, self-contained file. Install it from
[Greasy Fork](https://greasyfork.org/it/scripts/591989-item-helper-for-ogame); presentation and
discussion on the [OGame Origin forum](https://forum.origin.ogame.gameforge.com/forum/thread/558-item-helper-for-ogame).

> **Status: tolerated by the OGame Origin team.** The tool works next to premium content (shop
> items, Dark Matter purchases and activations), so on its first use it shows a notice about that,
> which you must accept before it does anything; the "i" button in the box shows it again. See
> [CHANGELOG.md](CHANGELOG.md).

## Install

1. Install [Tampermonkey](https://www.tampermonkey.net/).
2. Open [Item Helper for OGame on Greasy Fork](https://greasyfork.org/it/scripts/591989-item-helper-for-ogame)
   and press "Install this script".

## Screenshots

![Screenshot 1](https://i.ibb.co/Vp5GqkwX/schermata-20261020-171344.png)
![Screenshot 2](https://i.ibb.co/gL6y9J1D/schermata-20261020-171249.png)
![Screenshot 3](https://i.ibb.co/ycRtDKmZ/schermata-20261020-171203.png)
![Screenshot 4](https://i.ibb.co/yFdskhhZ/schermata-20261020-171138.png)
![Screenshot 5](https://i.ibb.co/0j80Q1mw/schermata-20261020-171107.png)

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
