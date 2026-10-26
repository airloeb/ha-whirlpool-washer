# Whirlpool Appliances — AWS washer preview

A temporary stand-in for Home Assistant's built-in **Whirlpool Appliances** integration, for newer Whirlpool/Maytag washers that the built-in one can't see yet ("No supported appliances found", [home-assistant/core#151547](https://github.com/home-assistant/core/issues/151547)).

It is the built-in integration from Home Assistant **2026.10.4**, with the [whirlpool-sixth-sense](https://github.com/abmantis/whirlpool-sixth-sense) library bundled at the unreleased washer branch ([abmantis/whirlpool-sixth-sense#224](https://github.com/abmantis/whirlpool-sixth-sense/pull/224), commit `f29c2a2`). Two small changes in `sensor.py`: the detergent-level sensor is skipped for washers that can't report it, and the end-time sensor tolerates a missing time remaining.

Read-only: washer state (including wash/rinse/spin phases), door, and cycle end time. Remove this once Home Assistant ships washer support for the new Whirlpool backend.

Library code is MIT licensed (see `custom_components/whirlpool/sixth_sense/LICENSE`); integration code is Apache-2.0 from [home-assistant/core](https://github.com/home-assistant/core).
