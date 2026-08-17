# EV System Monitoring and ADAS Dashboard using STM32

A real-time embedded system project developed during my **Emertxe internship**, focused on vehicle parameter monitoring and ADAS-related visualization using an **STM32 Blue Pill**, **PICSimLab**, and a **Python dashboard**.

The main idea behind this project was to understand how data from a vehicle can be collected by a microcontroller, processed in real time, and then presented to the user through a dashboard.

---

## 🚗 Project Overview

Modern vehicles continuously monitor different parameters such as speed, temperature, battery-related information, and surrounding conditions.

In this project, I worked on a small-scale implementation of a similar concept using an **STM32 Blue Pill** as the main controller.

The STM32 collects and processes the required vehicle information. The data is then communicated to a computer, where a **Python-based dashboard** displays the information in a user-friendly format.

The project also uses **PICSimLab** for simulation and testing of the embedded system.

The overall system can be represented as:

```text
       Vehicle / Sensor Inputs
                │
                ▼
        ┌─────────────────┐
        │   STM32 Blue    │
        │      Pill       │
        └────────┬────────┘
                 │
                 │ Serial Communication
                 ▼
        ┌─────────────────┐
        │ Python Dashboard│
        └────────┬────────┘
                 │
                 ▼
       Vehicle Monitoring
          & ADAS Display
```

---

## 🎯 Objectives

The main objectives of this project were:

* Understand the working of a real-time embedded vehicle monitoring system.
* Interface and process different input parameters using STM32.
* Develop embedded firmware for the STM32 microcontroller.
* Understand serial communication between the embedded system and PC.
* Develop a Python dashboard for real-time visualization.
* Simulate and test the system using PICSimLab.
* Understand the basic working concept of ADAS-related monitoring and warnings.
* Gain practical experience in debugging an embedded system from the firmware level to the user interface.

---

## 🛠️ Hardware Used

* STM32 Blue Pill
* STM32F103C8T6 microcontroller
* Sensor/input modules as required by the system
* LEDs / indicators
* USB-to-Serial interface where required
* Computer for Python dashboard and simulation

---

## 💻 Software and Tools

### Embedded Development

* Embedded C
* STM32 development environment
* STM32F103C8T6
* GPIO
* ADC
* Timers
* UART / Serial communication

### Simulation

* PICSimLab

### Dashboard

* Python
* Python GUI/dashboard libraries
* Serial communication

---

## 🔧 System Working

The system is divided into three major parts:

### 1. Data Acquisition

The STM32 acts as the main controller.

Input information is acquired through the connected peripherals/sensors. The microcontroller processes this information according to the application requirements.

---

### 2. Data Processing and Communication

After receiving the input data, the STM32 processes the values and prepares the information for transmission.

The processed data is sent to the PC through serial communication.

This creates a simple communication path:

```text
Input
  ↓
STM32
  ↓
Data Processing
  ↓
UART / Serial
  ↓
PC
```

---

### 3. Python Dashboard

The Python application receives the data from the STM32 and presents it through a dashboard.

Instead of looking at raw serial data, the user can monitor the vehicle information in a more understandable visual format.

The dashboard is intended to make the system easier to monitor and understand in real time.

---

# 🧠 ADAS Concept

One of the important learning areas of this project was understanding the basic concept behind **Advanced Driver Assistance Systems (ADAS)**.

ADAS systems use information from sensors and other vehicle systems to assist the driver.

In this project, the focus was on understanding how:

```text
Sensor / Vehicle Data
        ↓
Microcontroller
        ↓
Data Processing
        ↓
Decision / Warning
        ↓
Driver Dashboard
```

The project helped me understand the relationship between embedded systems, real-time data processing, vehicle monitoring, and driver information systems.

---

# 🖥️ Python Dashboard

The Python dashboard acts as the monitoring interface.

The general flow is:

```text
STM32
  │
  │ Serial Data
  ▼
Python Application
  │
  ├── Receive Data
  ├── Process Data
  ├── Update Values
  └── Display Information
```

The dashboard makes it easier to observe the system without directly monitoring the microcontroller's internal data.

---

# 🧪 PICSimLab Simulation

**PICSimLab** was used as part of the simulation and testing process.

Simulation was useful for understanding the system behavior before/alongside hardware implementation.

The simulation workflow can be represented as:

```text
Firmware
   ↓
Microcontroller Simulation
   ↓
Input Changes
   ↓
System Response
   ↓
Dashboard / Output
```

This also helped in debugging the interaction between the embedded firmware and the monitoring interface.

---

# 🔌 Communication

Serial communication is an important part of this project.

The STM32 communicates the processed information to the Python application.

A simplified representation is:

```text
STM32 TX  ─────────────►  PC / Python
STM32 RX  ◄─────────────  PC / Python
```

The Python application reads the incoming serial data and updates the dashboard.

The exact communication format depends on the firmware implementation.

---


# ▶️ How to Run the Project

## STM32 Firmware

1. Clone this repository.

```bash
git clone https://github.com/YOUR_USERNAME/EV-ADAS-Dashboard-STM32.git
```

2. Open the STM32 project in the appropriate STM32 development environment.

3. Connect the STM32 Blue Pill.

4. Build the project.

5. Flash the firmware to the STM32.

6. Connect the required serial interface to the PC.

---

## Python Dashboard

Navigate to the dashboard directory:

```bash
cd Python_Dashboard
```

Install the required Python packages:

```bash
pip install -r requirements.txt
```

Run the dashboard:

```bash
python dashboard.py
```

Select the appropriate serial/COM port and start the application.

> The exact commands and Python dependencies may vary depending on the final dashboard implementation.

---

# 🧪 Testing

Testing was carried out by checking the system at different levels.

### Firmware Testing

* Peripheral initialization
* GPIO operation
* Sensor/input reading
* Data processing
* UART communication

### Communication Testing

* Checking transmitted data
* Checking received data
* Verifying data format
* Checking communication reliability

### Dashboard Testing

* Checking serial data reception
* Checking parameter updates
* Checking dashboard response
* Verifying displayed values

### Simulation Testing

* Testing system behavior in PICSimLab
* Checking input/output responses
* Debugging firmware behavior before final integration

---

# 🐛 Debugging and Learning

One of the most useful parts of this project was debugging.

The project was not only about writing code. It involved understanding why a system was not behaving as expected and checking each part individually.

The debugging approach was:

```text
Problem
  ↓
Check Hardware
  ↓
Check Peripheral
  ↓
Check Firmware
  ↓
Check Communication
  ↓
Check Python Application
  ↓
Identify Root Cause
  ↓
Fix and Test Again
```

This helped me develop a better understanding of practical embedded-system debugging.

---

# 📚 Key Concepts Learned

Through this project, I gained practical exposure to:

* STM32 microcontrollers
* Embedded C
* GPIO configuration
* ADC concepts
* Timers
* UART communication
* Real-time data handling
* Microcontroller debugging
* PICSimLab simulation
* Python serial communication
* Dashboard development
* Vehicle monitoring concepts
* Basic ADAS concepts
* Hardware-software integration
* System-level debugging

---

# 🚀 Future Improvements

This project can be extended in several ways.

Some possible improvements are:

* Add CAN communication for a more automotive-oriented architecture.
* Add more vehicle parameters.
* Improve the dashboard UI.
* Add data logging.
* Store vehicle data for later analysis.
* Add graphical plots for historical parameters.
* Add more ADAS warning functions.
* Add fault detection and diagnostic information.
* Replace simulated inputs with real automotive sensors.
* Develop a more advanced HMI similar to an actual vehicle instrument cluster.

---

# 📸 Project Images

Screenshots and photographs of the project can be found in the `Images` directory.

Example:

### Hardware Setup

Add your STM32/hardware photograph here.

### PICSimLab Simulation

Add your simulation screenshot here.

### Python Dashboard

Add your final dashboard screenshot here.

---

# 🎓 Internship Project

This project was developed as part of my **Emertxe internship**, where I gained practical exposure to embedded-system development and worked on understanding the complete flow from microcontroller-level programming to a PC-based monitoring interface.

The project helped me connect theoretical ECE concepts with practical embedded development.

---

# 👨‍💻 Author

**Ganta Bhaskara Sri Satya Balaji**

B.Tech – Electronics and Communication Engineering

Interested in:

* Embedded Systems
* Automotive Electronics
* STM32
* ESP32
* Embedded C/C++
* RTOS
* PCB Design
* IoT
* Vehicle Electronics




