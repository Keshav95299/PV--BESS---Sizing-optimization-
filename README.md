# Results: effect of design lifetime

The table shows the optimal installed capacities selected by the model for each tested planning horizon. Costs, input profiles and other parameters are held fixed; replacement charges are triggered according to component lifetime.

| Design lifetime (years) | PV capacity (kWp) | Battery capacity (kWh) | Converter capacity (kW) | Objective cost (EUR) |
|---|---:|---:|---:|---:|
| 3 | 0 | 0 | 0 | 98,660 |
| 5 | 0 | 0 | 0 | 164,360 |
| 7 | 0 | 0 | 0 | 230,060 |
| 10 | 0 | 0 | 0 | 328,620 |
| 20 | 0 | 169.23 | 46.382 | 629,940 |
| 22 | 84.2354 | 74.4301 | 28.4695 | 710,856.8352 |

## Interpretation

**3-10 years:** The model selects no new PV, battery or converter capacity. Within these tested horizons and assumptions, investment does not reduce the modeled objective below the available no-investment alternative.

**20 years:** The model selects a 169.23 kWh battery and a 46.382 kW converter, with no PV. Grid charging is permitted, so storage can operate without solar generation. Electricity-price-driven charging and discharging can explain its value, but individual dispatch decisions require examining prices and operating constraints.

**22 years:** The model selects 84.2354 kWp of PV, 74.4301 kWh of battery storage and a 28.4695 kW converter. Relative to the 20-year case, PV appears and the selected storage and converter capacities are smaller. More operating years and replacement-cost changes jointly affect the result.

## How to read these results

- A zero capacity is a valid investment decision, not solver failure.
- The objective is the implemented lifetime cost, not profit or payback. Raw totals across different horizons should not be used to rank profitability.
- These cases do not identify the exact horizon at which PV first becomes attractive; the 21-year case was not tested.
- Values are transcribed from the author's demonstrated MATLAB output. Earlier objective values and some capacities were rounded in the source screenshot; the displayed decimal places are not a claim of additional precision.
- Results apply to the documented modified scenario and its simplified peak-charge, replacement and degradation accounting. They are not a validated investment recommendation.

[Download the numerical table](reference/screenshot_results.csv).

The `generated/` subfolder is reserved for fresh exports from the packaged MATLAB script. The reported table above is based on the supplied demonstration, not a new run.
