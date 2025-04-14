# Exploratory Data Analysis
Different plots will be used to understand and evaluate the data in the classes.

## Box Plots for each Sensor
![Box Plot for Sensor 1](../Images/EE461_PEMFC_boxPlot_P1.png)
**Figure1: Box plot for sensor one**

- The box plot of the first sensor is identical with the box plot of sensors 2,3 and 4.
- It is note worthy as Inter Quartile range i limited to zero. 
- This shows that the values recorded by these sensors are extremely identical and thus **not useful for a classification problem**

![alt text](<../Images/Box Plot for Sensor 5.png>)
**Figure 02: Box Plot for Sensor 5 showing comparison between the 3 classes**

- The values int he faulty region are extremely varied with numerous outliers.
    - This could be a result of transient loads or unstable conditions.
- The normal operation is tightly bound  around a certain value (105).
- The unknown data is also spread out mid-range.
- Such a variance in classes are good for classification problems.
- Similar variance can  be observed in the remaining sensors.

##