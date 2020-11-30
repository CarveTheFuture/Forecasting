# Forecasting models based on time-series data
When procuring or maintaining machinery, it is useful to know how much life is left on the component parts or on the composite system.
On some machinery, it is not a reasonable option to allow the machine to go past the time when a preventive maintenance is needed. 
Dangerous accidents and costly damage have resulted when such a mistake was made.
Yet maintenace costs can be very expensive.
Thus, cost can be reduced by not having the maintenance done too early, while also ensuring that the maintenance is done before it is too late.

The CMAPSS engine aircraft dataset from NASA was used to demonstrate a method for estimating remaining useful life.

A dataframe was created by reading the 4 training csv files and appending each, in python.


100 units were subjected to this modeling.
When a certain threshold on the sensor measurements was reached, it was inferred that the units had departed from optimal operational windows. Then the model was halted.

Shown below are the details of the dataframe containing the dataset.


class 'pandas.core.frame.DataFrame'>
103150 entries, 0 to 20629
Data columns (total 28 columns):
| 0            | unit        | number      |        |
|--------------|-------------|-------------|--------|
|              |             |             |        |
| 1            | time,       | in          | cycles |
|              |             |             |        |
| 2            | operational | setting     | 1      |
|              |             |             |        |
| 3            | operational | setting     | 2      |
| 4            | operational | setting     | 3      |
| 5            | sensor      | measurement | 1      |
| 6            | sensor      | measurement | 2      |
| 7            | sensor      | measurement | 3      |
| 8            | sensor      | measurement | 4      |
| 9            | sensor      | measurement | 5      |
| 10           | sensor      | measurement | 6      |
| 11           | sensor      | measurement | 7      |
| 12           | sensor      | measurement | 8      |
| 13           | sensor      | measurement | 9      |
| 14           | sensor      | measurement | 10     |
| 15           | sensor      | measurement | 11     |
| 16           | sensor      | measurement | 12     |
| 17           | sensor      | measurement | 13     |
| 18           | sensor      | measurement | 14     |
| 19           | sensor      | measurement | 15     |
| 20           | sensor      | measurement | 16     |
| 21           | sensor      | measurement | 17     |
| 22           | sensor      | measurement | 18     |
| 23           | sensor      | measurement | 19     |
| 24           | sensor      | measurement | 20     |
| 25           | sensor      | measurement | 21     |
| 26           | sensor      | measurement | 22     |
| 27           | sensor      | measurement | 23     |

As shown above, the first column was elapsed cycles in seconds.

The next 3 columns represented:
The varied operational settings

The last 23 columns represented the sensor measurements.
The following columns, upon closer examination were found to contain a single line or null values


| 26           | sensor      | measurement | 22     |
| 27           | sensor      | measurement | 23     |
