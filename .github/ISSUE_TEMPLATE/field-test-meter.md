---
name: 📏 Field test - Meter asset
about: Field test a new Meter asset type
title: "Field test <asset>"
labels: ["field-test-new-asset-type", "sales&ops", "enhancement"]
---

# Field Test: Meter

- [ ] The installation instructions listed in the documentation are sufficient for the installer and an operations engineer to connect the asset, and updated if not.
- [ ] The asset generates reports at the expected interval.
- [ ] The generation duration of the reports is not unexpectedly high, e.g. usually less than a couple hundred milliseconds.
- [ ] Energy increase roughly matches the active power over the elapsed time, at least 5 minutes.
- [ ] The voltage and current roughly equal the active power, both per phase and total.
- [ ] The frequency is between 49.8 Hz and 50.2 Hz.
- [ ] All other data entries have sensible values, e.g. no unexpected `null` values. Copy the JSON from the report in the field test ticket and e.g. add checkmarks (✅) and notes to each item for validation.
- [ ] The direction of current and power is the same.
- [ ] The active power roughly matches the expected power, both in magnitude and direction.  
  Tested by doing one of the following:
  1. Controlling another, already validated, asset connected to the Teleport. E.g. curtailing solar and observing a 50 kW jump down in active power and comparing that with the difference observed at the meter.
  2. A secondary measurement performed by a party on site. E.g. reading another meter, using a current clamp or multimeter to verify the current, etc.
- [ ] The asset connector TODOs have been dealt with and removed, or at least a PR open to do so.
- [ ] Documented any particularities (e.g., slow response times, required manual settings, or limitations) in the [asset guide](https://github.com/withthegrid/teleport/tree/main/guides/asset).
- [ ] Removed the `warning` on the public installation instructions about the field test not yet being completed.

