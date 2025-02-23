

---

# **Design and Simulation of a Dual Port Line Antenna in Ansys HFSS**

## **Introduction**
A **Dual Port Line Antenna** is widely used in RF and microwave applications such as **wireless communication, IoT devices, and radar systems**. In this project, we design and simulate a **dual port antenna** using **Ansys HFSS**, focusing on **geometry, material properties, excitation ports, and S-parameter analysis**.

![Line Antenna](https://github.com/user-attachments/assets/f8ba0ce7-3807-4076-be41-2968ec378931)

---

## **Antenna Structure and Design**
The **Dual Port Line Antenna** consists of:
1. **FR4 Substrate**
2. **Ground Plane**
3. **Radiating Patch**
4. **Feed Line**
5. **Lumped Ports**
6. **Radiation Boundary**

Each component is defined with precise **positioning and dimensions**.

---

### **1. FR4 Substrate**
The **FR4 substrate** acts as the dielectric medium for the antenna.

| **Property**  | **Value**  |
|--------------|-----------|
| **Command**  | CreateBox |
| **Position** | (0, 0, 0) mm |
| **XSize**    | 20 mm |
| **YSize**    | 40 mm |
| **ZSize**    | 1.6 mm |



---

### **2. Ground Plane**
The **ground plane** provides a conductive layer for proper antenna performance.

| **Property**  | **Value**  |
|--------------|-----------|
| **Command**  | CreateBox |
| **Position** | (-10, -10, -20) mm |
| **XSize**    | 40 mm |
| **YSize**    | 60 mm |
| **ZSize**    | 40 mm |



---

### **3. Radiating Patch**
The **patch** is the main radiating element of the antenna.

| **Property**  | **Value**  |
|--------------|-----------|
| **Command**  | CreateRectangle |
| **Position** | (10, -1.5, 1.6) mm |
| **Axis**     | Z |
| **XSize**    | 3 mm |
| **YSize**    | 40 mm |



---

### **4. Feed Line**
The **feed line** provides the excitation for the antenna.

| **Property**  | **Value**  |
|--------------|-----------|
| **Command**  | CreateRectangle |
| **Position** | (8.5, 0, 1.6) mm |
| **Axis**     | Y |
| **XSize**    | 3 mm |
| **ZSize**    | -1.6 mm |



---

### **5. Lumped Ports**
The **lumped ports** provide the excitation source for the antenna.

#### **Lumped Port 1**
| **Property**  | **Value**  |
|--------------|-----------|
| **Command**  | CreateRectangle |
| **Position** | (8.5, 0, 1.6) mm |
| **Axis**     | Y |
| **XSize**    | 3 mm |
| **ZSize**    | -1.6 mm |



#### **Lumped Port 2**
| **Property**  | **Value**  |
|--------------|-----------|
| **Command**  | CreateRectangle |
| **Position** | (11.5, 40, 1.6) mm |
| **Axis**     | Y |
| **XSize**    | -3 mm |
| **ZSize**    | -1.6 mm |



---

### **6. Radiation Boundary**
The **radiation boundary** ensures that the simulation replicates real-world free-space conditions.

| **Property**  | **Value**  |
|--------------|-----------|
| **Command**  | CreateBox |
| **Position** | (-10, -10, -20) mm |
| **XSize**    | 40 mm |
| **YSize**    | 60 mm |
| **ZSize**    | 40 mm |



---

## **Simulation and S-Parameter Analysis**
After designing the **Dual Port Line Antenna**, an **S-parameter sweep** was performed to evaluate its **performance across different frequencies**.

### **S-Parameter Results**
The S-parameters (**S11, S21, S22**) indicate:
- **Reflection Loss (S11, S22)**: How much power is reflected back.
- **Transmission Coefficient (S21)**: How much power is transferred between ports.

_Image of S-Parameter Plot:_  

![Result - S parameter at each port](https://github.com/user-attachments/assets/57afb5cb-f110-459c-bc32-dd73eb10f511)

#### **Key Observations**
- **S11 (Port 1 Reflection Coefficient)**: Indicates how well the antenna is impedance matched.
- **S21 (Power Transfer between Ports 1 & 2)**: Shows coupling between ports.
- **S22 (Port 2 Reflection Coefficient)**: Measures reflection at Port 2.

From the plot, the antenna demonstrates multiple resonance points, indicating good performance over a wide frequency range.

---

## **Advantages and Applications**
### **Advantages**
✅ **Compact and Lightweight** – Ideal for modern communication systems.  
✅ **Broadband Performance** – Operates over multiple frequency bands.  
✅ **Cost-Effective** – Uses **FR4 substrate**, making it an economical choice.  

### **Applications**
📡 **Wireless Communication (Wi-Fi, Bluetooth, RFID)**  
📡 **IoT and Smart Devices**  
📡 **5G and MIMO Antenna Systems**  
📡 **Satellite and Radar Communication**  

---

## **Conclusion**
The **Dual Port Line Antenna** designed in **Ansys HFSS** demonstrates efficient radiation characteristics and strong performance in S-parameter analysis. The **multiple resonances** indicate that this antenna is suitable for **wideband applications**.

To further improve performance, consider:
- **Optimizing patch and feed dimensions** for better resonance.
- **Using a different substrate (e.g., Rogers 4003)** for enhanced dielectric properties.
- **Adding a matching network** for better impedance matching.

---

## **Future Work**
🔹 Try modifying the **patch shape** (e.g., circular, triangular) to study its effects.  
🔹 Experiment with different **substrates** to analyze gain and efficiency variations.  
🔹 Implement **parasitic elements** to improve bandwidth and directivity.  

---

