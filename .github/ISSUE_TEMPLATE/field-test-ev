---
name: 📏 Field test - EV asset
description: Field test a new EV asset type
title: "Field test <asset>"
labels: ["field-test-new-asset-type", "sales&ops", "enhancement"]
---

# Field Test: EV

- [ ] The installation instructions listed in the documentation are sufficient for the installer and an operations engineer to connect the asset, and updated if not.
- [ ] The asset generates reports at the expected interval.
- [ ] The generation duration of the reports is not unexpectedly high, e.g. usually less than a couple hundred milliseconds.
- [ ] The direction of all current and power measurements is correct.
- [ ] Voltage values are within expected ranges.
- [ ] The status of the cars is correctly reported according to IEC standards: `vehicleConnected` and `isCharging` are correctly inferred from the car status.
- [ ] Checked that the energy increase roughly matched the active power multiplied by the elapsed time, at least 5 minutes.
- [ ] The active power measurement roughly matches an external reference source. 
  Tested by doing one of the following:
  1. Verified against a separate meter.
  2. Verified via a reading from the web interface or screen of the asset, as provided by the installer, asset owner, or operator.
- [ ] The asset accepts and correctly applies charging limits when a car is connected:
  - The asset responds within a few seconds and reaches the target active power with a small margin. Most EVs should respond to setpoints within 5–10 seconds.
  - When limited to 0, no car starts charging.
- [ ] There are no alarms.
- [ ] All other data entries have sensible values, e.g. no unexpected `null` values and sensible values in `inverters`. Copy the JSON from the report in the field test ticket and e.g. add checkmarks (✅) and notes to each item for validation.
- [ ] The asset accepts a setpoint and the read back setpoint in the reports matches the sent setpoint.
- [ ] The asset can be controlled, i.e. the active power output of the asset roughly matches the setpoint after a couple of seconds.
- [ ]  When uncontrolled, the setpoint goes back to the default setpoint, unlimited, after a couple of seconds and the active power increases.
- [ ] The asset connector TODOs have been dealt with and removed, or at least a PR open to do so.
- [ ] Documented any particularities (e.g., slow response times, required manual settings, or limitations) in the [asset guide](https://github.com/withthegrid/teleport/tree/main/guides/asset).
