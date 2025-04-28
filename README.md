# GNSS RTK for Automated Guided Vehicles (AGV)

This program is developed for research projects related to Automated Guided Vehicles (AGV). It involves cooperation in the development of several components. This software is designed to extract satellite data using [GNSS-RTK](https://www.ardusimple.com/product/simplertk2blite/) and process it to create accurate routes for AGVs.

<img align="left" src="https://github.com/SupakunZ/GNSS_RTK/assets/168329218/2add411e-2949-45cb-b9d4-d89d171c66ce" style="padding-right:30px;" alt="status" height="365" width="375"/> <img src="https://github.com/SupakunZ/GNSS_RTK/assets/168329218/afb75c6a-a79c-47ee-b603-5051c42cdbf8" alt="status" width="375"/>

## 🏆 Project Overview

This project focuses on using GNSS-RTK to assist in guiding AGVs along predetermined routes with high accuracy. The data is processed to track AGV position, plot paths on maps, and determine distances to target points. The program is designed for real-time navigation and provides feedback when the AGV is within proximity to a target point.

## 🛠 Architecture & Workflow

<img src="https://github.com/user-attachments/assets/3f394eb2-ac82-40a7-889c-a365678110f2" alt="Flow Chart" width="770"/>

The program's architecture consists of the following main components:

- **GNSS-RTK Receiver**: The SimpleRTK2B Lite is used to receive satellite data.
- **Data Processing**: The software processes data to extract latitude, longitude, and other relevant information.
- **AGV Path Planning**: The program creates accurate paths based on GNSS data, ensuring the AGV follows a designated route.
- **GUI Interface**: The Tkinter-based GUI visualizes AGV position on a map, displays real-time coordinates, and tracks progress toward target points.

The workflow follows these steps:
1. **Connect** the GNSS-RTK receiver to the computer for data collection.
2. **Process** the satellite signals according to the NMEA 0183 standard.
3. **Display** the current latitude and longitude on a map and update the AGV's position.
4. **Calculate** the distance between the AGV's current position and target points.
5. **Move** the AGV along the planned path, triggering an update when it reaches a target within a specified radius.

## 🔄 Flow Chart

<img src="https://github.com/SupakunZ/GNSS_RTK/assets/168329218/4323387b-3ea9-4794-96f7-649031daab41" alt="Flow Chart" width="770"/>

The flow chart shows the step-by-step operation of the program, divided into two main parts:

1. **Data Collection & Display**
    - Connect the SimpleRTK2B Lite device to the computer.
    - Receive and display satellite data (latitude, longitude, and number of satellites).
    - Export the collected data to a text file.
  
2. **AGV Path Navigation**
    - Ensure the SimpleRTK2B Lite device is properly connected to avoid errors.
    - The map visualizes the AGV's position and generates a route.
    - The AGV follows the path, updating when it reaches a target point within a 4-meter radius.

## 📦 Requirements

- **Software**:
  - Ubuntu 20.04 LTS (required)
  - Python 3.8.10 (recommended)

- **Hardware**:
  - SimpleRTK2B Lite

## 📈 How to Use

1. **Clone this repository**:

```bash
git clone https://github.com/SupakunZ/GNSS_RTK.git
```

2. **Navigate to the project folder**:

```bash
cd GNSS_RTK
```

3. **Install dependencies as detailed in the `Documentation.pdf`**

4. **Run the program**:
    - Make sure the SimpleRTK2B Lite device is connected.
    - Use the GUI to track AGV position and monitor real-time data.
    - Set target points for the AGV to follow.


## 🌼 Base example
<img src="https://github.com/SupakunZ/GNSS_RTK/assets/168329218/9268214f-fe91-43cf-80f7-509b2f3b1daa" alt="status" width="770"/> 
<img align="left" style="padding-right:30px;" src="https://github.com/SupakunZ/GNSS_RTK/assets/168329218/3b4154c6-2a84-4a3f-b54c-d913a07f8d61" alt="settings" width="375"/> <img src="https://github.com/SupakunZ/GNSS_RTK/assets/168329218/2f557904-337d-44e0-9ca6-9c1b032f753d" alt="settings" width="375"/>

## 📁 File Structure
- `GNSS_RTK/`: The main directory for the project.
  - `documentation/`: Documentation files for installation and usage.
  - `src/`: Source code for the GNSS-RTK program.
  - `data/`: Contains files for data storage and logs.
  - `tests/`: Testing files and test results.

## 🌟 Features

  - **Real-time AGV Position Tracking**: The program tracks the AGV's position using GNSS data and displays it on a map.
  - **Route Creation**: Automatically generates paths for the AGV to follow based on GNSS data.
  - **Map Display Options**: Users can switch between different map views, such as OpenStreetMap and Google Maps.
  - **Proximity Alerts**: Alerts when the AGV is within a specified distance (10 meters) of the target point.

## 💎 Result 

https://github.com/user-attachments/assets/b0f40eee-3261-4058-8d7f-4c03f1580003

## 📚 Documentation

- 📄 **`Documentation.pdf`** – Detailed instructions for installing the program.  
- 📄 **`Appendix.pdf`** – Installation guides for third-party tools used in this project.  
- 📹 **`Result GnssRTK.mp4`** – Demonstration video, located in the `tests/` folder.

