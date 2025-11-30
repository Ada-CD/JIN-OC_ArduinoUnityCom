# Arduino↔Unity communication example

This is a simple Unity project that communicates with an Arduino board, used in the context
of a course teaching the basics of Arduino.  

This was last tested using the `6000.0.63f1` version of Unity.

---

The board controls the state of a river blocking the way and the speed of pressure plate timers,
allowing Unity to turn the built-in LED on when both timers are active at the same time !

It uses the `SerialPort` class provided by the .NET framework in `System.IO.Ports`,
but wrapped in order to handle disconnections and I/O errors easily.  
**Check that the project is using .NET 4 in the player settings in Unity** !

The Arduino code is contained in the [Arduino_Controller](Arduino_Controller) folder.  
It cannot be moved out, otherwise the Arduino IDE will complain and force you to create the folder.

---

It also features an example communication via TCP/IP between a WiFi enabled ESP8266 board and a Unity script.  
The Arduino file is in [Arduino_Wifi](Arduino_Wifi) and the Unity side is handled by `TCPHandler.cs`.  
The Arduino echoes back what it receives on the serial port while the Unity script uses `Debug.Log`.
