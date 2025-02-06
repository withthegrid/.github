---
name: 📏 Field test - Battery asset
about: Field test a new Battery asset type
title: "Field test <asset>"
labels: ["field-test-new-asset-type", "sales&ops", "enhancement"]
---

# Field Test: Battery

- [ ] The installation instructions listed in the documentation are sufficient for the installer and an operations engineer to connect the asset, and updated if not.
- [ ] The asset generates reports at the expected interval.
- [ ] The generation duration of the reports is not unexpectedly high, e.g. usually less than a couple hundred milliseconds.
- [ ] There are no alarms.
- [ ] Verified the direction of all current and power measurements, including for DC measurements.
- Set a low (e.g., 10% of nominal power) charging setpoint and confirmed that:
- [ ] State of Charge (SoC), energy.charged, and availableEnergy increased.
- [ ] Energy.discharged remained constant.
- [ ] Active power and current measurements became negative.
- [ ] Checked that the energy and SoC increase roughly matched the active power multiplied by the elapsed time, at least 5 minutes.
- [ ] Compared the active power measurement with an external source by doing one of the following:
  1. Reading an already validated meter connected to the Teleport. E.g. charging the battery with 20 kW and observing -20 kW active power on the battery, and comparing that with the difference observed at the meter.
  2. Reading the active power via the web interface or screen of the asset, the latter being read by a party on site.
- [ ] Checked the direction and magnitude of reactive power: set a reactive power setpoint on the asset and verified that the appropriate change occurred on the measured reactive power on the meter.
- Set a dispatch power setpoint as large as possible while staying well within grid limits:
- [ ] Tested both charging and discharging directions.
- [ ] Confirmed the asset responds within a few seconds and reaches the target active power with a small margin.
- [ ] Updated [`ALLOWED_AUXILIARY_CONSUMPTION_PERCENTAGE_MARGIN`](https://github.com/withthegrid/teleport/blob/e0519b583602216d3f91105520a4a3952ffc54e2/packages/cloud-device-gateway/src/services/monitors/active-power-is-responsive.ts#L35).
- [ ] Updated `DEFAULT_STATE_OF_CHARGE_LIMITS`.
- [ ] The asset connector TODOs have been dealt with and removed, or at least a PR open to do so.
- [ ] Documented any particularities (e.g., slow response times, required manual settings, or limitations) in the [asset guide](https://github.com/withthegrid/teleport/tree/main/guides/asset).
