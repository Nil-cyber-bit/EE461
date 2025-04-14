# 📊 DATASET DESCRIPTION

To study the condition of the **PEMFC**, data from various sensors monitoring the system are utilized. The sensor data is divided into three classes:

1. ✅ **Normal Sensor Data**
2. ⚠️ **Faulty Sensor Data**
3. ❓ **Unknown Sensor Data**

Throughout this project, they will be referred to as **normal**, **faulty**, or **unknown**.

---

## ✅ Normal Sensor Data

- Recorded during steady-state operation under constant load current.  
- Indicates healthy system performance without any recorded faults.  
- Represents baseline behavior of the PEMFC with consistent sensor readings.

---

## ⚠️ Faulty Sensor Data

- Occurs during periods of **transient load current**, which often cause operational issues.
- Accompanied by system errors such as:
  - 💧 Membrane drying out  
  - 🔋 Hydrogen supply issues  
- Clearly identifiable by:
  - Distinct changes in sensor readings  
  - Activation of system error indicators

---

## ❓ Unknown Sensor Data

- Also recorded under transient load current, similar to faulty data.  
- No faults are flagged by the system, and no error indicators are activated.  
- Considered **ambiguous**:
  - Mimics faulty behavior in load variation  
  - Reflects a healthy state upon deeper analysis  
- Used to **challenge** the diagnostic system’s ability to distinguish false positives.

---

# 🗃️ Data Preview


![Preview of the dataset table showing rows of labeled data](https://github.com/user-attachments/assets/05711649-3494-4b0d-b4ba-092a8337b3fe)

*Figure 1: Preview of Excel data for one class*

---

# 🧪 Sensor Description

| 🧾 **Sensor Measurement**          | 📐 **Unit** |
|-----------------------------------|-------------|
| Stack Voltage                     | V           |
| Load Current                      | A           |
| Anode Reactant Flow               | SLPM        |
| Anode Inlet Pressure #1           | mbar        |
| Anode Inlet Pressure #2           | mbar        |
| Anode Outlet Pressure #1          | mbar        |
| Anode Outlet Pressure #2          | mbar        |
| Cathode Air Inlet Flow            | SLPM        |
| Water Inlet Temperature           | °C          |
| Primary Water Inlet Pressure #1   | mbar        |
| Primary Water Inlet Pressure #2   | mbar        |
| Cathode Inlet Pressure #1         | mbar        |
| Cathode Inlet Pressure #2         | mbar        |
| Cathode Outlet Pressure #1        | mbar        |
| Cathode Outlet Pressure #2        | mbar        |
| Cathode Stoichiometry             | N/A         |
| Cathode Inlet Temperature #1      | °C          |
| Cathode Inlet Temperature #2      | °C          |
| Cathode Outlet Temperature #1     | °C          |
| Cathode Outlet Temperature #2     | °C          |
| Primary Water Inlet Flow #1       | SLPM        |
| Primary Water Inlet Flow #2       | SLPM        |

---

# 🎯 Purpose of the Sensors

- 🔌 **Stack Voltage** and **Load Current** reflect the system's electrical output.
- 🧪 **Anode Inlet/Outlet Pressure Sensors** measure pressure changes as hydrogen flows through the anode.
- 💨 **Cathode Air Inlet Flow Sensor** monitors the oxygen supplied to the cathode.
- 🌡️ **Water Inlet Temperature Sensor** ensures cool water enters to regulate system temperature.
- 💧 **Primary Water Inlet Pressure Sensors** measure incoming water pressure (in SLPM).
- ⚙️ **Cathode Inlet/Outlet Pressure Sensors** monitor and regulate air pressure entering/leaving the cathode.
- 🌬️ **Cathode Inlet/Outlet Temperature Sensors** measure the temperature of air flowing through the cathode.
- ⚖️ **Cathode Stoichiometry Sensor** calculates the required oxygen-to-hydrogen ratio for each fuel cell reaction.

---

