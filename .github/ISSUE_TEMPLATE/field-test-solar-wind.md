---
name: 📏 Field test - Solar & Wind asset
about: Field test a new Solar or Wind asset type
title: "Field test <asset>"
labels: ["field-test-new-asset-type", "sales&ops", "enhancement"]
---

# Field Test: Solar and Wind Assets

- [ ] The installation instructions listed in the documentation are sufficient for the installer and an operations engineer to connect the asset, and updated if not.
- [ ] The asset generates reports at the expected interval.
- [ ] The generation duration of the reports is not unexpectedly high, e.g. usually less than a couple hundred milliseconds.
- [ ] The active power roughly matches the expected power.  
  Tested by doing one of the following:
  1. Reading an already validated meter connected to the Teleport. E.g. curtailing solar and observing a 50 kW reduction in active power and comparing that with the difference observed at the meter.
  2. Reading the active power via the web interface or screen of the asset, the latter being read by a party on site.
- [ ] The energy increase roughly matches the average active power value multiplied by the elapsed time (if active power fluctuates heavily, curtailed the asset to just below the lowest fluctuation point).
- [ ] There are no alarms.
- [ ] All other data entries have sensible values, e.g. no unexpected `null` values and sensible values in `inverters`. Copy the JSON from the report in the field test ticket and e.g. add checkmarks (✅) and notes to each item for validation.
- [ ] The asset accepts a setpoint and the read back setpoint in the reports matches the sent setpoint.
- [ ] The asset can be controlled, i.e. the active power output of the asset roughly matches the setpoint after a couple of seconds.
- [ ] When uncontrolled, the setpoint goes back to the default setpoint, unlimited, after a couple of seconds and the active power increases.
- [ ] The asset connector TODOs have been dealt with and removed, or at least a PR open to do so.
- [ ] Documented any particularities (e.g., slow response times, required manual settings, or limitations) in the [asset guide](https://github.com/withthegrid/teleport/tree/main/guides/asset).
