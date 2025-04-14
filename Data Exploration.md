# Exploratory Data Analysis
Different plots will be used to understand and evaluate the data in the classes.

## Box Plots for each Sensor
![EE461_PEMFC_boxPlot_P1](https://github.com/user-attachments/assets/4e3625a4-157f-4e6a-bf90-1a7c6178b596)
*Figure1: Box plot for sensor one*

- The box plot of the first sensor is identical with the box plot of sensors 2,3 and 4.
- It is note worthy as Inter Quartile range i limited to zero. 
- This shows that the values recorded by these sensors are extremely identical and thus **not useful for a classification problem**

![Box Plot for Sensor 5](https://github.com/user-attachments/assets/543fc4d2-fa5e-4b74-889f-bf7e42f2fc48))
*Figure 02: Box Plot for Sensor 5 showing comparison between the 3 classes*

- The values int he faulty region are extremely varied with numerous outliers.
    - This could be a result of transient loads or unstable conditions.
- The normal operation is tightly bound  around a certain value (105).
- The unknown data is also spread out mid-range.
- Such a variance in classes are good for classification problems.
- Similar variance can  be observed in the remaining sensors.

## Correlation Plots
### Understanding Correlation

- **Positive Correlation (value close to +1)**
    - Redundant senors that may be measuring the same phenomenon.
    - Sensors recording similar data, reading are functionally linked.
- **Negative Correlation (value close to -1)**
    - As one senor value increases the other sensor value decreases
    - Sensors with opposing roles in the system.
    - This should be expected for every pair of sensor as each pair is measuring input and output of the system.
- **Near-Zero Correlation (value close to 0)**
    - No constant linear relationship.
    - these sensors monitor totally different subsystems.

**For classification problems we require lower correlations as they would suggest that the sensors are providing unique signals which is valuable for classifying diverse data**

![Correlation Plot of the 20 Sensors in the normal state](https://github.com/user-attachments/assets/cae65abb-d2c9-469b-8f6b-5ea21aeab348)
*Figure 03: Correlation Plot of  Sensor data in Normal Operation*

![Correlation Plot of the 20 Sensors in the Faulty state](https://github.com/user-attachments/assets/cd5b4cbe-bded-45a1-a35f-b5b5a83a8580)
*Figure 03: Correlation Plot of  Sensor data during Faulty Operation*

![Correlation Plot of the 20 Sensors in the Unknown state](https://github.com/user-attachments/assets/d361d4e6-fd2f-4fa1-8726-3dcb9d09baf2)

*Figure 03: Correlation Plot of  Sensor data in Unknown State of Operation*
## Observations
- S1 to S4 are redundant as can be observed form the plot.
    - The correlation value is NaN since the division by the Standard deviation is 0.
    - This is possible if all the values are the same.
- Considering S1 to S4 contain the same values they are not useful for classification problems.
- **Color Bar** shows that lower correlations values will be in shades of blue. 
    - Lower correlation values indicate uniqueness in data.
    - This can be observed in  Normal Operation and Unknown operation.
- The faulty states shows sensors recording similar values as color analysis indicates most values are positively correlated.
    - Tis could be because the system is operating in extreme condition and all the sensors are recording extreme values simultaneously.
