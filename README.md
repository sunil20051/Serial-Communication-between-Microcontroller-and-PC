# Send and receive data between a microcontroller (Arduino/ESP32) and a PC.

Exp 4 Send and receive data between a microcontroller (Arduino/ESP32) and a PC.


**Aim**

To send and receive data between an Arduino UNO microcontroller and a PC using serial communication through the Arduino IDE Serial Monitor.

**Apparatus Required**

•	Arduino UNO
•	USB cable
•	Computer/PC
•	Arduino IDE

**Circuit / Connection**

Connect the Arduino UNO to the PC using a USB cable. No external circuit is required.
 
<img width="602" height="195" alt="image" src="https://github.com/user-attachments/assets/a94ea03e-7454-4215-bcba-6dd280cb0988" />


**Procedure**
1.	Connect the Arduino UNO to the PC using the USB cable.
2.	Open Arduino IDE and select Arduino UNO and the correct COM port.
3.	Enter and upload the program given below.
4.	Open the Serial Monitor and set the baud rate to 9600.
5.	Observe the message sent from Arduino to the PC.
6.	Enter a message in the Serial Monitor and observe the received message.

**Arduino IDE Code**
```c
void setup() {
  Serial.begin(9600);
  Serial.println("Hello from Arduino");
}

void loop() {
  // Send data from Arduino to PC
    // Receive data from PC
  if (Serial.available() > 0) {
    char receivedData = Serial.read();

    Serial.print("Received: ");
    Serial.println(receivedData);
  }

  delay(1000);
}
```

**Output:**

<img width="1280" height="960" alt="image" src="https://github.com/user-attachments/assets/5b296dd9-9e6a-4589-a660-c0b5f1b429f0" />

**Serial Monitor output**

<img width="1600" height="960" alt="image" src="https://github.com/user-attachments/assets/698b369c-d17a-4c6b-a0c3-6213b7d8f2c8" />

**Result**

Data was successfully sent and received between the Arduino UNO and the PC using serial communication through the Arduino IDE Serial Monitor


