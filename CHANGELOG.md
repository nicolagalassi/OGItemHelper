# Changelog

## 1.3.4

- **Items gone from the shop are no longer offered:** event items that left the shop stayed in the
  list as "Buy" and could not be found when clicked. Every read of the shop tab now drops what the
  shop no longer sells; such items still show if you own them or have them active.

## 1.3.3

- **Expiring copies get their own card:** copies of an item with a deadline are no longer merged
  with the copies of the same item that have none. Before, 1 expiring + 7 undated showed as one
  card "×8 ⏳ 6h", as if all eight were about to expire; now they are two cards, ×1 with the
  deadline and ×7 without.

## 1.3.2

- **Time-left badges off by default:** the timers on active items and officers now appear only
  after switching them on in Settings (⚙). A choice already made in Settings is kept.

## 1.3.1

- **Bogus filter chips fixed:** the category labels could be picked up from unrelated page
  elements, showing chips made of resource figures or coordinates. Labels now come only from the
  game's own category buttons and links, anything with digits is refused, and the labels stored
  by older versions are discarded and learned again.

## 1.3.0

- **Notice on premium content**, asked for by the OGame Origin team with the toleration. The first
  time the tool is used, the shop shows only a notice that the tool interacts with premium content
  (items, purchases and activations with Dark Matter); the tool does nothing — no box, no overview
  reminder, no time-left badges — until the player presses "I understand". The answer is stored in
  the browser (`localStorage`), so it is asked once. Afterwards the "i" button in the box shows the notice
  again. It is in the player's interface language (IT/EN/DE/FR/ES/PL/TR/PT/RU), English otherwise.
- **Language fallback fixed:** an interface in a language the tool does not speak (e.g. Romanian)
  now gets English. Before, it kept the last supported language seen (Spanish stayed Spanish).

## 1.2.0

- Filter chips on the game's own inventory categories, plus "expiring" and "active".
- Settings panel (⚙) for the display flags, the "expiring soon" threshold and the deadline colours.

## 1.1.1

- Time left written on the active items and under the officers, on every page.
- Nine languages: IT/EN/DE/FR/ES/PL/TR/PT/RU.
- One-click durations.

## 1.0.0

- First release: searchable inventory box on the shop page, active items on this planet, durations
  grouped under one button, jump to the same item on the next planet, deadline reminder on the
  overview.
