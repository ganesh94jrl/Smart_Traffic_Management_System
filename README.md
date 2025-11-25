# **📘 SMART TRAFFIC MANAGEMENT SYSTEM**

### *Automated Ambulance Clearance | Pollution Monitoring | Solar-Powered Signals 

---

## **🔍 Overview**

The **Smart Traffic Management System** is an intelligent, Arduino-based solution designed to overcome challenges in modern traffic control. It integrates **ambulance priority clearance, pollution detection, pedestrian safety controls, and solar-powered operation** into a unified system.

The goal is to reduce congestion, enhance emergency response, monitor environmental pollution, and ensure uninterrupted traffic signal operation—even during power failures.

This project uses **Arduino Uno, IR sensors, CO₂ sensors, LEDs, a solar charging system, relays, and rechargeable batteries**, all integrated through **Embedded C**.

---

## **📂 Features**

### ✅ **Ambulance Priority System**

* IR transmitter on ambulance sends signal to junction.
* Traffic light instantly turns **green for ambulance lane** and **red for all others**.
* System resumes normal mode automatically.

### ✅ **Pollution Detection**

* MQ-135 sensor detects CO₂ and harmful gases.
* Buzzer alerts public when pollution crosses threshold.

### ✅ **Pedestrian Safety System**

* Push-button activates safe crossing interval.
* Vehicles stop until pedestrian crossing completes.

### ✅ **Solar-Powered Smart Signals**

* Solar panel charges 6V battery for 24/7 operation.
* Voltage regulator ensures stable 5V supply for controller and sensors.

### ✅ **Fully Automated Traffic Light Control**

* Four-lane signal control using Red/Yellow/Green LEDs.
* Emergency override & stable timing management.

---

## **🛠️ Hardware Components**

| Component                                    | Purpose                              |
| -------------------------------------------- | ------------------------------------ |
| **Arduino Uno**                              | Central controller for entire system |
| **IR Sensor Module**                         | Detects ambulance IR signal          |
| **IR LED Transmitter**                       | Mounted on ambulance                 |
| **MQ-135 Gas Sensor**                        | Monitors CO₂ and pollutants          |
| **Traffic LEDs (R/Y/G)**                     | Four-lane traffic signal output      |
| **Solar Panel (12V)**                        | Renewable energy source              |
| **Lead-Acid Battery (6V)**                   | Stores power from solar panel        |
| **7805 Voltage Regulator**                   | Provides stable 5V supply            |
| **PCB Board**                                | Hardware integration                 |
| **Buzzer**                                   | Pollution alert output               |
| **Relay Module**                             | Power switch & isolation             |
| **Transformers, Diodes & Filter Capacitors** | AC-DC conversion & power regulation  |

---

## **🧠 Software Requirements**

### **Arduino IDE**

* Used to write, compile, and upload Embedded C code.
* Handles all traffic logic, emergency logic, sensors, and timing.

### **DipTrace PCB Designer**

* Used for schematic design and PCB layout.
* Helps create manufacturable circuit boards.

---

## **⚙️ System Working (Methodology)**

1. **Normal Mode (Traffic Cycle)**

   * Each lane receives Red → Yellow → Green sequence.
   * Controlled by Arduino via digital pins.

2. **Ambulance Detection**

   * Ambulance IR signal is captured by IR receiver.
   * Arduino overrides normal traffic cycle.
   * Ambulance lane turns **Green instantly**.
   * All other lanes turn **Red**.
   * Once ambulance passes, system returns to standard mode.

3. **Pollution Monitoring**

   * MQ-135 continuously checks air quality.
   * If CO₂ level > preset limit → buzzer alerts.

4. **Pedestrian Button Mode**

   * Pressing button halts traffic.
   * Displays safe "Walk" indication.
   * After timeout, normal cycle resumes.

5. **Solar Power Operation**

   * Solar panel charges 6V battery via rectifier circuit.
   * Battery feeds voltage regulator → stable 5V to Arduino.
   * Ensures uninterrupted operation even during power failures.

---

## **🧾 Arduino Code (Uploaded File Summary)**

Your code includes:

* Lane-wise actions (`lane1action()`, `lane2action()`…)
* Emergency override functions
* Sensor checks for all lanes
* Timed delay-based traffic logic
* Digital control of LED signals

This logic accurately matches the real-world four-way traffic junction behavior.

---

## **📊 Testing & Results**

### ✔ Traffic Light Testing

* Stable LED operation without flickering.
* Correct 3-second switching cycle.

### ✔ Ambulance System Testing

* Immediate lane clearance upon IR signal detection.
* Smooth return to normal mode afterward.

### ✔ Pollution System Testing

* High CO₂ triggers alarm instantly.
* Reliable threshold-based detection.

### ✔ Solar Power & Battery Testing

* Battery charges properly under sunlight.
* 7805 regulator provides consistent 5V output.

### ✔ Pedestrian System Testing

* Safe crossing intervals executed correctly.

---

## **💡 Advantages**

* Instant ambulance clearance
* Reduced congestion
* Low energy consumption via solar power
* Continuous pollution monitoring
* Highly reliable and automated system
* Cost-effective and easy to implement

---

## **⚠️ Limitations**

* IR-based detection requires line-of-sight
* No real-time traffic density counting
* Sensor aging can affect accuracy
* Solar efficiency reduces in low-light conditions
* Limited data analytics due to Arduino memory

---

## **🚀 Future Scope**

* IoT & cloud connectivity for centralized control
* GPS-based ambulance tracking
* AI/ML for adaptive traffic timing
* Multi-junction synchronization
* Integration with V2I (Vehicle-to-Infrastructure)
* Additional environmental sensors (PM2.5, PM10, NO₂)
* Lithium-ion based energy storage & MPPT controllers

---

## **📷 Project Image**

*(As shown in your PDF)*
A full model prototype with traffic lights, solar panel, sensors, Arduino controller, and wiring system.

---

## **📚 References**

Includes IEEE papers, research articles, and traffic management system publications (as provided in your PDF).


Just tell me — I can generate it instantly.
