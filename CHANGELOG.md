# Changelog

## 1.0.1

### Changes
- Smarter exclude lists in the visual editors: the Sensors, Lights and Plugs cards only offer the entities they find in the chosen room, with their own rules (sensors of the right kind without the camera detections, lights without light groups, plugs without light switches); the Overview card only offers the rooms it finds. Entities and rooms already excluded stay in the list. The exclude list appears once a room is chosen.

## 1.0.0

First release of **ha-room-card**: the room cards in a single HACS download.

### What's new
- Four cards in one file, `ha-room-card.js`: `room-overview-card`, `room-sensors-card`, `room-lights-card` and `room-switch-card`. The card types are unchanged, so dashboards using the former room-sensors-card, room-lights-card or room-switch-card repositories keep working.
- **Overview** (new): one compact tile per room, coloured by what matters most (leak, open, presence), with chips for the lights and plugs that are on and the power drawn; header with the home status and totals; tap a room to unfold its Sensors, Lights and Plugs cards at the top of the card, tap again or anywhere else to fold it back. `rooms` for the order, names, icons or a `navigation_path`, `exclude_areas`, `only_active`, `sort: state`.
- **Sensors**: leak, door, window, opening and presence sensors of a room (from room-sensors-card 1.1.2): open sensors first with how long they have been open, presence in blue, camera detections left out; `only_alerts`, `hide_when_clear` (hidden only when everything is closed and dry and nobody is there), `presence`, `blink`.
- **Lights**: lights and light switches of a room (from room-lights-card 1.0.1): tap to toggle, drag to dim, hold for details, colour and brightness on the tile, turn everything off from the pill.
- **Plugs**: smart plugs of a room with their power draw (from room-switch-card 1.0.1): tap to toggle, hold for details, total power in the header, optional turn-everything-off.
- Same visual editor options wording on every card, labels in English and French, light and dark themes.
