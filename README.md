# Autonomous Drone Star Mission using MAVSDK & PX4

This project demonstrates autonomous drone mission planning using **MAVSDK-Python** and the **PX4 Autopilot** ecosystem. The script programmatically calculates relative geographic offsets to fly a precise star-like geometric path, monitored and simulated in real-time using **QGroundControl** and **JMAVSim**.

---

## 📸 Simulation Preview

The image below displays the active workspace workflow showing the Python script execution, QGroundControl flight path tracking, and the JMAVSim 3D simulator environment:

![Star Mission Simulation](Star%20mission%20Using%20a%20compass.jpg)

---

## 🛠️ Mission Architecture & Parameters

### MissionItem Parameter Layout
Every coordinate point or command action in the flight path is defined as a `MissionItem`. Based on the project's internal structural logic, these arguments can be grouped into 4 main categories:

```python
# MissionItem(Navigation, Movement, Camera Angles, Safety & Aircraft State)
