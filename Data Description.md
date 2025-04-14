# DATASET DESCRIPTION
To study the condition of the **PEMFC** the data from the sensors monitoring hte condition is utilized. The sensor data is divided into three classes.
1. Normal Sensor Data
2. Faulty Sensor Data
3. Unknown Sensor Data
Through out this project they will be refered to as normal, faulty or unknown.

## Normal  Sensor Data
- Recorded during steady-state operation under constant load current.

- Indicates healthy system performance without any recorded faults.

- Represents baseline behavior of the PEMFC with consistent sensor readings.

## Faulty Sensor Data
- Occurs during periods of transient load current, which often cause operational issues.

- Accompanied by system errors, such as:
    - Membrane drying out
    - Hydrogen supply issues

- Clearly identifiable due to distinct changes in sensor readings and activation of error indicators.

## Unknown Sensor Data
-Also recorded under transient load current, similar to faulty data.

- No faults are flagged by the system, and no error indicators are activated.

- Considered ambiguous, as it mimics faulty behavior in terms of load variation but reflects a healthy state upon analysis.

- Used to challenge the diagnostic system’s ability to distinguish false positives.

# Data Preview
![Preview of the dataset table showing rows of labeled data](Images/datasetPreview.png)

*Figure 1: Preview of excel data for on class*

# Sensor Description
| **Sensor measurement**          | **Unit** |
|---------------------------------|----------|
| Stack Voltage                   | V        |
| Load current                    | A        |
| Anode reactant flow             | SLPM     |
| Anode inlet pressure #1         | mbar     |
| Anode inlet pressure #2         | mbar     |
| Anode outlet pressure #1        | mbar     |
| Anode outlet pressure #2        | mbar     |
| Cathode air inlet flow          | SLPM     |
| Water inlet temperature         | °C       |
| Primary water inlet pressure #1 | mbar     |
| Primary water inlet pressure #  | mbar     |
| Cathode inlet pressure #1       | mbar     |
| Cathode inlet pressure #2       | mbar     |
| Cathode outlet pressure #1      | mbar     |
| Cathode outlet pressure #2      | mbar     |
| Cathode stoichiometry           | N/A      |
| Cathode inlet temperature #1    | °C       |
| Cathode inlet temperature #2    | °C       |
| Cathode outlet temperature #1   | °C       |
| Cathode outlet temperature #2   | °C       |
| Primary water inlet flow #1     | SLPM     |
| Primary water inlet flow #2     | SLPM     |

# Purpose of the  Sensors
- Stack voltage and load current refer to the voltage and current at the system's output.

- Anode inlet/outlet pressure sensor measures pressure changes as hydrogen enters and exits the anode.

- Cathode air inlet flow sensor monitors the oxygen supplied to the cathode.

- Water inlet temperature sensor detects the temperature of incoming water to help regulate system cooling.

- Primary water inlet pressure sensors measure the pressure of the incoming water.

    - These pressure sensors measure in SLPM (Standard Liters Per Minute).

- Cathode inlet and outlet pressure sensors regulate and monitor air pressure entering and exiting the cathode.

- Cathode inlet and outlet temperature sensors measure the temperature of air entering and leaving the cathode.

- Cathode stoichiometry sensor determines the oxygen-to-hydrogen ratio required for each reaction.
