IoT-Based Soil Moisture Monitoring System Using ThingSpeak

1. Project Objectives

- To measure the moisture level in soil using a soil moisture sensor.
- To interface the soil moisture sensor with an ESP8266 Wi-Fi development board.
- To monitor soil moisture readings remotely using the ThingSpeak IoT cloud platform.
- To display sensor readings and estimated moisture percentage.
- To understand the application of Internet of Things (IoT) in smart agriculture and plant monitoring.

2. Components Required

- ESP8266 NodeMCU Wi-Fi development board
- Soil moisture sensor module
- Jumper wires
- Breadboard (if required)
- USB cable for programming and power
- Computer with Arduino IDE
- Wi-Fi connection
- ThingSpeak account

3. Working Principle

The soil moisture sensor detects the moisture level in the soil and produces an electrical signal corresponding to the sensor reading.

The ESP8266 reads the sensor's analog output through its analog input pin. The program uses the sensor reading to calculate an estimated soil moisture percentage based on calibrated dry and wet values.

Using its Wi-Fi connection, the ESP8266 sends the sensor reading and estimated moisture percentage to the ThingSpeak cloud platform.

ThingSpeak displays the received data in the form of charts, allowing the user to monitor soil moisture remotely.

4. Technologies Used

- Embedded C/C++: For writing the microcontroller program.
- Arduino IDE: For writing, compiling, and uploading the code.
- ESP8266 Wi-Fi: For wireless internet connectivity.
- ThingSpeak IoT Platform: For cloud-based data storage, visualization, and monitoring.
- Analog Sensor Interfacing: For reading soil moisture sensor values.
- Internet of Things (IoT): For connecting the hardware to an online monitoring platform.

5. Expected Output

- Read soil moisture sensor values.
- Calculate an estimated moisture percentage.
- Send the readings to ThingSpeak over Wi-Fi.
- View the uploaded readings on a ThingSpeak dashboard.

6. Applications

- Smart agriculture
- Garden and plant monitoring
- Greenhouse monitoring
- Soil moisture observation for irrigation planning
- IoT-based environmental monitoring

7. Project Status

Source code has been uploaded to GitHub. Hardware testing and verification of ThingSpeak readings will be documented after testing.

8. Source Code

See "soil_moisture_monitor.ino" in this repository.
