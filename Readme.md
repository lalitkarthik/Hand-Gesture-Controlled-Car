# Hand Gesture Controlled Car

This project demonstrates how to control a car using hand gestures detected through a webcam. The system consists of three main components:

1. **ESP8266 WiFi Module**: For establishing a WiFi connection and creating a server.
2. **Python Script**: For detecting hand gestures and sending corresponding commands to the ESP8266.
3. **Arduino Car Mechanism**: For receiving commands from the ESP8266 and controlling the car's movements.

## Components
- ESP8266 WiFi Module
- Arduino Board
- Motor Driver (AFMotor)
- Webcam
- Python (with OpenCV and cvzone)

## Setup Instructions

### 1. ESP8266 Setup
Upload the provided code to your ESP8266 to establish a WiFi connection and create a server. This code handles the communication between the ESP8266 and the Arduino via SoftwareSerial.

### 2. Python Script
Run the provided Python script to detect hand gestures using OpenCV and cvzone. The script captures video from your webcam, detects hand gestures, and sends corresponding commands to the ESP8266 server.

### 3. Arduino Car Mechanism
Upload the provided code to your Arduino to receive commands from the ESP8266 and control the car's motors. The Arduino code includes functions to move the car forward, backward, left, right, and stop based on the received commands.

## How It Works

### ESP8266 WiFi Module
- Connects to the specified WiFi network.
- Creates a server to listen for incoming connections and commands.
- Forwards received commands to the Arduino via SoftwareSerial.

### Python Script
- Uses a webcam to capture video and detect hand gestures.
- Translates detected hand gestures into commands (e.g., forward, backward, left, right, stop).
- Sends commands to the ESP8266 server over a socket connection.

### Arduino Car Mechanism
- Receives commands from the ESP8266.
- Controls the car's motors using the AFMotor library based on the received commands.

## Commands
The following commands are recognized by the system:
- `f;` - Move forward
- `b;` - Move backward
- `l;` - Turn left
- `r;` - Turn right
- `s;` - Stop

## Video Demonstration

(https://github.com/lalitkarthik/Hand-Gesture-Controlled-Car/blob/main/Model%20image.jpg)

(https://github.com/lalitkarthik/Hand-Gesture-Controlled-Car/blob/main/Working%20model.mp4)

## Conclusion
This project showcases the integration of computer vision, networking, and embedded systems to create a hand gesture-controlled car. It can be extended with additional features and improvements, such as more complex gestures and improved motor control.

