🌿 Greenhouse Automation and Monitoring System🌿

An IoT-based smart greenhouse solution that allows real-time monitoring and automation of environmental conditions like temperature, humidity, soil moisture, and fire detection. It also provides voice control and web-based control for turning ON/OFF lights and fans using NodeMCU, Python GUI, and Arduino.

📌 Features

🔥 Fire detection using a flame sensor (Arduino)
💧 Soil moisture monitoring (Arduino)
🌡️ Temperature and Humidity monitoring using DHT11 (NodeMCU)
💡 Control Lights & Fans via:
          - Python GUI Interface
          - Voice commands using Speech Recognition
          - Web Dashboard hosted on NodeMCU
☁️ Weather Information from OpenWeatherMap API
🗣️ Voice Assistant powered by macOS AppKit (with speech feedback)
📱 Responsive Bootstrap Web UI served directly from NodeMCU


🧰 Components Used
- Hardware:
- NodeMCU (ESP8266)
- Arduino Uno
- DHT11 Temperature and Humidity Sensor
- Soil Moisture Sensor
- Flame Sensor
- Relay Module (if controlling real AC appliances)
- LEDs, Fan (DC or symbolic)
- Power Supply

Software/Platforms:
- Arduino IDE
- Python 3.x
- Tkinter (GUI)
- SpeechRecognition Library
- AppKit (macOS voice synthesis)
- OpenWeatherMap API
- HTML/CSS (Bootstrap) for Web UI


🖥️ System Architecture

          [Sensors]              [NodeMCU]
           🔥 Flame ------------> Reads & Sends Data
           💧 Moisture ----------> Hosts Web Dashboard
                                  |
        [Python GUI/Voice] <---- Uses HTTP commands to control
                                  |
               🗣️ Voice Recognition, Weather API

               
🚀 How to Set Up

1. NodeMCU Setup (ESP8266)
Flash the .ino file using Arduino IDE.
Replace WiFi credentials in code:
WiFi.begin("Your_SSID", "Your_PASSWORD");
Ensure the DHT sensor and GPIOs are wired correctly.


2. Arduino Setup
Upload the flame and soil moisture monitoring code.
Connect sensors to respective analog and digital pins.
Serial Monitor can be used for real-time detection logs.


3. Python Voice GUI Setup
Ensure Python 3.x is installed.
Install dependencies:
pip install speechrecognition requests AppKit
Modify IP address (root_url) to match your NodeMCU local IP.
Run the Python script:
python greenhouse_gui.py


4. Web UI
Access via browser using NodeMCU IP (e.g., http://192.168.123.1)
Control Light and Fan using on-page buttons.
🎤 Voice Commands Supported
"Turn on light", "Turn off fan", etc.
"Check weather"
"Shutdown"
"Hey buddy" / "Jarvis" – wakes assistant
Friendly responses to "How are you", "Thank you", etc.


📝 Future Improvements
Add data logging to Firebase/Google Sheets
Add real-time charts for temperature and moisture
Mobile app integration
Plant-specific watering algorithms


🧑‍💻 Authors
- Project by: Aman Kumar sah , Bijaya Giri, Mukesh kumar sah, Prem shrestha 
- Campus: IOE Purwanchal Campus, Dharan
- Departments: Electronics, Communication & Information Engineering
