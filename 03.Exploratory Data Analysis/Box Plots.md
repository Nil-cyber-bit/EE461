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

- The values in the faulty region are extremely varied with numerous outliers.
    - This could be a result of transient loads or unstable conditions.
- The normal operation is tightly bound  around a certain value (105).
- The unknown data is also spread out mid-range.
- Such a variance in classes are good for classification problems.
- Similar variance can  be observed in the remaining sensors.


- The faulty states shows sensors recording similar values as color analysis indicates most values are positively correlated.
    - Tis could be because the system is operating in extreme condition and all the sensors are recording extreme values simultaneously.
