# SmartBin Setup Guide

## Overview

This guide explains how to assemble, connect, and upload the SmartBin project to an Arduino UNO.

---

## Hardware Requirements

| Component                 | Quantity    |
| ------------------------- | ----------- |
| Arduino UNO               | 1           |
| HC-SR04 Ultrasonic Sensor | 1           |
| SG90 Servo Motor          | 1           |
| Breadboard                | 1           |
| Jumper Wires              | As Required |
| USB Cable                 | 1           |

---

## Software Requirements

* Arduino IDE (latest version recommended)
* Servo Library (included with Arduino IDE)

---

## Circuit Connections

### HC-SR04 Ultrasonic Sensor

| HC-SR04 Pin | Arduino UNO Pin |
| ----------- | --------------- |
| VCC         | 5V              |
| GND         | GND             |
| TRIG        | D9              |
| ECHO        | D10             |

### SG90 Servo Motor

| Servo Pin | Arduino UNO Pin |
| --------- | --------------- |
| Signal    | D11             |
| VCC       | 5V              |
| GND       | GND             |

Refer to:

```text
Docs/Circuit_Diagram.png
```

for the complete wiring diagram.

---

## Project Setup

### Step 1: Install Arduino IDE

Download and install the Arduino IDE from:

https://www.arduino.cc/en/software

---

### Step 2: Open the Project

Open:

```text
Src/SmartBin_Code.ino
```

using Arduino IDE.

---

### Step 3: Select Board

Navigate to:

```text
Tools → Board → Arduino AVR Boards → Arduino UNO
```

---

### Step 4: Select COM Port

Connect the Arduino board using a USB cable.

Navigate to:

```text
Tools → Port
```

and select the appropriate COM port.

---

### Step 5: Verify the Code

Click:

```text
✔ Verify
```

to compile the project.

---

### Step 6: Upload the Code

Click:

```text
→ Upload
```

to flash the program to the Arduino UNO.

---

## Working Procedure

1. Power on the Arduino UNO.
2. The ultrasonic sensor continuously measures distance.
3. When a hand or object comes within the detection range, the sensor sends data to the Arduino.
4. The Arduino activates the servo motor.
5. The dustbin lid opens automatically.
6. After a short delay, the lid closes.
7. The system waits for the next object detection event.

---

## Troubleshooting

### Servo Not Moving

* Check servo wiring.
* Verify signal wire is connected to the correct pin.
* Ensure adequate power supply.

### Ultrasonic Sensor Not Detecting Objects

* Verify TRIG and ECHO pin connections.
* Check sensor orientation.
* Confirm wiring matches the circuit diagram.

### Upload Failed

* Ensure the correct COM port is selected.
* Verify Arduino UNO is selected as the board.
* Disconnect and reconnect the USB cable.

---

## Project Files

```text
SmartBin
│
├── Assets
├── Docs
│   ├── Circuit_Diagram.png
│   ├── Project_Report.pdf
│   └── setup_guide.md
│
├── Hardware
│   └── components_list.md
│
├── Src
│   └── SmartBin_Code.ino
│
└── README.md
```

---

## Author

K. Nithin Kumar Goud

Bachelor of Engineering (Electronics and Communication Engineering)
