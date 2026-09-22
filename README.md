# Drop Me

## Overview

This project analyzes Drop Me machine operations and transaction data to identify reliability issues, understand material rejection patterns, and predict which machines are likely to need collection.

The final output is intended to support operations teams with a daily priority list rather than automatically making collection decisions.

## How to Run

1. Clone or download this repository.
2. Make sure the data files are available.
3. Install the required packages.
4. Open and run the notebook from start to finish.



## Packages Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn

## Important Assumptions

* Fill percentage should normally be between 0% and 100%.
* Machine IDs should be consistent across the two datasets.
* A collection need is based on the available operational data and should be treated as a prediction, not a guaranteed event.
* The ML model is intended to support operational decisions, not automatically dispatch trucks.

## Important Data Issues Found

Several data-quality issues were identified and addressed:

* Duplicate rows were found .
* Machine IDs contained inconsistent trailing spaces.
* Some fill-level readings were above 100%..
* Some uptime values appeared to be capped at exactly 82%, so uptime should be interpreted cautiously.

## Not Finished / Limitations

* The data covers only around 2.5 months and 14 machines.
* There is not enough historical data to properly assess seasonal, holiday, or weather effects.
* Route and truck information was not available, so the model predicts collection need but does not optimize collection routes.
* Sensor-health information was not available.

## What I Would Do Next

With more time, I would:

* Collect more historical data across different seasons and locations.
* Add truck, route, distance, and capacity information.
* Add sensor-health or self-diagnostic information.
* Investigate the high rejection rate for Aluminium and the 100% rejection of Unknown materials.
* Eventually combine collection prediction with route planning.

## AI-Assisted Work
AI assistance was used as a supporting tool during the project. It helped with some syntax and mathematical operations, as well as improving writing, wording, and presentation of the findings
