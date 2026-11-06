# SoliSCADA – Simulation-Based Solar PV Plant SCADA Monitoring System

**A Software-Based SCADA Simulation Project Using SOLISCADA Memory Driver**

## 1. Project Overview

SoliSCADA is a simulation-based Solar Photovoltaic (PV) Plant Supervisory Control and Data Acquisition (SCADA) monitoring project developed to understand and demonstrate the fundamental architecture and functionality of an industrial SCADA system.

The project was developed entirely on a computer using SOLISCADA software and its Memory Driver. Instead of connecting physical sensors, PLCs, or solar inverters, simulated tags and memory variables were created to represent important parameters of a solar power plant.

The objective was to understand how industrial SCADA systems acquire, organize, monitor, and visualize plant parameters through a software-based environment.

## 2. Project Objectives

- Understand the fundamentals of industrial SCADA architecture.
- Explore the SOLISCADA development environment.
- Create and configure a SCADA tag database.
- Understand different data types and memory addresses.
- Simulate important solar plant operating parameters.
- Develop a foundation for solar plant monitoring.
- Understand how SCADA databases, tag groups, alarms, and historical trends are organized.
- Establish a foundation for future integration with real-time plant data.

## 3. Technologies and Tools Used

| Technology | Purpose |
|---|---|
| SOLISCADA | SCADA development and monitoring environment |
| SOLISCADA Memory Driver | Simulating plant parameters |
| VxExplorer | Project configuration and management |
| Database Management | Creating and configuring SCADA tags |
| Tag Group Manager | Organizing monitoring variables |
| History Trend | Understanding historical data monitoring |
| Alarm Setting | Configuring alarm-related parameters |

**Project type:** Software-based simulation

**Hardware requirement:** No physical hardware used.

## 4. Understanding the Basics of SCADA

Before developing the project, it is important to understand the basic components of a SCADA system.

SCADA stands for Supervisory Control and Data Acquisition.

A typical industrial SCADA system consists of:

1. **Field Instruments:** Sensors and meters that measure physical parameters.
2. **PLC/RTU:** Collects field data and communicates with the SCADA system.
3. **Communication Network:** Transfers data between field devices and servers.
4. **SCADA Server:** Processes and manages incoming data.
5. **Database:** Stores real-time and historical information.
6. **HMI:** Provides a graphical interface for operators to monitor the plant.

In this project, the field instrumentation and PLC communication layers were represented using simulated memory variables.

## 5. Project Development – Step-by-Step Implementation

### Step 1: Exploring the SOLISCADA Environment

The first step was exploring the SOLISCADA development environment and understanding its available configuration modules.

The VxExplorer interface provides access to different project configuration sections.

The main sections explored include:

- Database
- Tag Group Manager
- Tag Second Confirm
- History Trend
- Pop Trend
- Electric Signature
- Supervising User Authority
- Alarm Setting
- Custom Alarm Group
- Database Source
- RTDataRestore
- EventSetting
- Schedule
- Recipe Management
- 3D Config
- Object Model
- Operation Team
- Resource Files

These modules provide the foundation for configuring and managing a SCADA application.

### Step 2: Creating the SCADA Database

The next step was creating the database required to store the simulated solar plant parameters.

Using the Database Management module, individual tags were created with the following attributes:

- Tag Name
- Data Type
- Description
- I/O Drive
- I/O Address

The Memory Driver was selected as the I/O Drive to simulate the data internally without requiring external hardware.

### Step 3: Understanding Data Types

Different data types were assigned depending on the nature of the parameter.

| Data Type | Application |
|---|---|
| Real | Decimal values such as power, temperature and efficiency |
| Integer | Whole-number values such as module efficiency |
| Switch | Binary status such as inverter ON/OFF |
| String | Text information such as date and time |

### Step 4: Creating Solar Plant Simulation Tags

The following tags were configured to represent important operating parameters of a solar PV plant.

| Tag Name | Description | Data Type |
|---|---|---|
| SIM_ACPower | AC Power of Inverter | Real |
| SIM_DCPower | DC Power of Inverter | Real |
| SIM_AmbientTemp | Ambient Temperature | Real |
| SIM_PanelTemperature | Panel Temperature | Real |
| SIM_Irradiance | Solar Irradiance | Real |
| SIM_DailyEnergy | Daily Energy Yield | Real |
| SIM_FDEY | Forecasted Daily Energy Yield | Real |
| SIM_CG | Current Generation | Real |
| SIM_CUF | Capacity Utilisation Factor | Real |
| SIM_Efficiency | Efficiency of Inverter | Real |
| SIM_INVefficiency | Inverter Efficiency | Real |
| SIM_PlantAvailability | Plant Availability | Real |
| SIM_GA | Grid Availability | Real |
| SIM_GridFreq | Grid Frequency | Real |
| SIM_QVAR | Reactive Power | Real |
| SIM_InverterStatus | Inverter Status | Switch |
| SIM_DateTime | Date and Time | String |
| SIM_CableLoss | Cable Loss | Real |
| SIM_TransformerLoss | Transformer Loss | Real |
| SIM_ShadingLoss | Shading Loss | Real |
| SIM_Soiling_Loss | Soiling Loss | Real |
| SIM_DegradationLoss | Degradation Loss | Real |
| SIM_SystemEfficiency | System Efficiency | Real |
| SIM_SystemLosses | System Losses | Real |
| SIM_PanelTemperature | Panel Temperature | Real |
| SIM_RainGauge | Rain Gauge | Real |

Additional tags were configured for transformer oil temperature, plant load factor, specific yield, mismatch loss and other performance parameters.

### Step 5: Configuring the Memory Driver

The Memory Driver was used to represent the input and output variables of the simulated plant.

Each tag was assigned a corresponding memory address in the database configuration.

The I/O Address column was configured using the address identifiers supported by the Memory Driver.

This approach allowed the project to represent different plant parameters without requiring physical sensors or external PLC connections.

### Step 6: Organizing the SCADA Project

After creating the database, the project structure was explored and organized through VxExplorer.

The available modules provide a framework for:

- Managing database tags.
- Organizing tag groups.
- Configuring alarm settings.
- Exploring historical trends.
- Managing event settings.
- Configuring project resources.
- Organizing SCADA objects.

### Step 7: Understanding Solar Plant Monitoring Parameters

The simulated parameters were selected to represent important aspects of solar power generation and plant performance.

Some important parameters include:

**Electrical Parameters**
- AC Power
- DC Power
- Reactive Power
- Grid Frequency

**Environmental Parameters**
- Solar Irradiance
- Ambient Temperature
- Panel Temperature
- Rain Gauge

**Performance Parameters**
- Inverter Efficiency
- Plant Availability
- Capacity Utilisation Factor
- Specific Yield
- System Efficiency

**Loss Parameters**
- Cable Loss
- Transformer Loss
- Shading Loss
- Soiling Loss
- Degradation Loss
- Mismatch Loss

These parameters provide a foundation for understanding how solar plant performance can be monitored through a SCADA system.

### Step 8: Testing and Validation

The project configuration was reviewed to verify the database structure, tag names, descriptions, data types and Memory Driver assignments.

The objective was to establish a functional software-based simulation environment and understand the relationship between database variables and SCADA monitoring functions.

## 6. Project Architecture

The conceptual architecture of SoliSCADA is:

```text
        SOLAR PV PLANT
              |
     Simulated Plant Parameters
              |
       SOLISCADA MEMORY
            DRIVER
              |
        SCADA DATABASE
              |
        TAG MANAGEMENT
              |
       SCADA MONITORING
              |
    +---------+---------+
    |         |         |
  Trends   Alarms   Performance
    |         |      Parameters
    +---------+---------+
              |
       PLANT MONITORING
```

*Note: This represents the conceptual architecture of the simulation. It does not represent an actual field-connected SCADA network.*

## 7. Key Learnings

Through this project, I gained practical software-based exposure to:

- SCADA system architecture and configuration.
- Industrial tag database management.
- Memory Driver configuration.
- Different SCADA data types.
- Solar PV plant operating parameters.
- Inverter and plant performance monitoring concepts.
- Alarm and historical trend configuration modules.
- SCADA project organization using VxExplorer.

## 8. Project Limitations

This project was developed entirely as a software-based simulation.

The following components were not physically integrated:

- Solar PV panels.
- Physical temperature and irradiance sensors.
- Actual solar inverters.
- PLCs or RTUs.
- Industrial communication networks.
- Live solar plant data sources.

The project focuses on understanding SCADA configuration, database management and simulation fundamentals rather than deploying a complete operational solar plant monitoring system.

## 9. Future Scope

The project can be extended further through:

1. Integration with real-time solar inverter data.
2. Modbus TCP/IP or Modbus RTU communication.
3. PLC-based data acquisition.
4. Real-time HMI dashboard development.
5. Advanced alarm management.
6. Historical generation analysis.
7. Solar plant performance deviation monitoring.
8. Predictive maintenance using machine learning.
9. Integration with actual plant SCADA data.

## 10. Conclusion

SoliSCADA provided an opportunity to explore the fundamentals of industrial SCADA development through a software-based solar plant simulation.

By creating simulated plant parameters, configuring database tags and exploring the different modules available in SOLISCADA, I developed a better understanding of how SCADA systems are structured and how plant parameters can be represented within a monitoring environment.

This project represents my initial step towards understanding renewable energy SCADA systems and their application in real-world solar power plants.

---

## Author

**Developed as an individual learning and project initiative by a SCADA Graduate Engineer Trainee.**

**Domain:** Renewable Energy | Solar SCADA | Industrial Automation

**Software:** SOLISCADA

**Project:** SoliSCADA – Simulation-Based Solar PV Plant SCADA Monitoring System

---

*This repository is intended for educational purposes and to document the step-by-step development of a software-based SCADA simulation project.*
