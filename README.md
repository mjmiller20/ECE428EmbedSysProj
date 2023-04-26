# ECE428EmbedSysProj

Low-Cost Residential Security Camera

Proposed Goals

At the onset of this project, we set out to solve the issue of creating a low-cost alternative to current commercial or residential solutions that both gave the end user granular control over their system and control over the telemetry data sent back to the manufacturer. 
The goals for this project included creating a prototype of a solution that connects to a Wireless LAN, transmits a video feed, reacts from a passive infrared sensor (PIR), and operate an RGB light remotely. 

Resources

During this project, I relied heavily on a project from (RandomNerdTutorials, 2020).
After getting this baseline to work, I worked heavily with the WiFi and httpd libraries to establish wide connections and operate a basic Web API from the device (Espressif, 2016).
For the PIR, I used basic information on the pins and the signal it would generate to make a basic script to handle the inputs to generate an output change (Last Minute Engineers, 2022).
Connecting the ESP32 required intimate knowledge of the ESP32-CAM GPIO pins and their functions as well, to communicate with the PIR and LED (RandomNerdTutorials, 2020).

Circuits

The circuit diagram is shown in Appendix A, and shows power connections to the ESP32 and PIR, with easy connection to a high-power LED as well as data lines to the LED and PIR. 

Code

A high-level flow chart showing the implementation on the ESP32 module is shown in Appendix B.
The code is dense with the implementation of the various libraries, but is found in Appendix C. 

Libraries

This project required usage of the ESP32 board library, including the esptool.py board programmer script with alterations to work with the latest version of Python 3. 

Results and Conclusion

With a series of tests, the module is functional and meets the requirements of the project set forth in the proposal, except for using a high-power floodlight RGB LED.
A low-level implementation of network attached-camera is produced with LAN-API access enabled for controls and information delivery.
There was a higher cost than expected, but still lower than many market alternatives, without compromising on data security.
Recommendations for future versions would include a different LED module with a higher output and an antenna to attach to the controller to extend the range and integrity of the WiFi connection.
Additional features could include an IR light and filter for night vision.
Implementation into market would require use of a high-level server or set-top box could then provide a User Interface for ease of access and implementation for the End User. 

References

https://docs.espressif.com/projects/esp-idf/en/latest/esp32/api-reference/protocols/esp_http_server.html
https://lastminuteengineers.com/pir-sensor-arduino-tutorial/
https://randomnerdtutorials.com/esp32-cam-ai-thinker-pinout/
https://randomnerdtutorials.com/esp32-cam-video-streaming-web-server-camera-home-assistant/

Appendix A
A model circuit diagram for the module showing connections to the ESP32 module, PIR sensor, and RGB LED.
<img width="468" alt="image" src="https://user-images.githubusercontent.com/43389618/234488796-ec9830b4-1346-41d3-bcee-4313183c3830.png">

Appendix B
A high-level flowchart of the program loaded onto the ESP32 Module.
<img width="419" alt="image" src="https://user-images.githubusercontent.com/43389618/234488935-9ac4b57e-3174-40c8-ba58-b5b7853c6016.png">

Appendix C
The code loaded to the ESP32 Module deigned to handle API calls for the camera feed, PIR sensing, and light controls.
Refer to this repository.
