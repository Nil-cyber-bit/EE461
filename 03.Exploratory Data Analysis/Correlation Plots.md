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
# Correlation Between Senosrs In A Class

![Correlation Plot of the 20 Sensors in the normal state](<Correlation Plot of Normal.png>)
*Figure 03: Correlation Plot of  Sensor data in Normal Operation*

![Correlation Plot of Faulty](https://github.com/user-attachments/assets/4e9f5ac5-f836-4ade-a5df-b65c26770a91)

*Figure 03: Correlation Plot of  Sensor data during Faulty Operation*


![Correlation Plot of Unknown](https://github.com/user-attachments/assets/d32d1a10-e018-43ba-866d-437c68f3b8d2)


*Figure 03: Correlation Plot of  Sensor data in Unknown State of Operation*
## Observations
- S1 to S4 are redundant as can be observed they were remvoed during normalization.
- Considering S1 to S4 contain the same values they are not useful for classification problems.
- **Color Bar** shows that lower correlations values will be in shades of blue. 
    - Lower correlation values indicate uniqueness in data.
    - This can be observed in  Normal Operation and Unknown operation.

---

# Correlation Between Sensors and Class
