# Traffic_lights
📘 Project Description (Short)  A simple Traffic Light System using Arduino Uno that simulates real-world traffic signals using LEDs. The system cycles through Red → Yellow → Green with timed delays. Perfect for beginners learning Arduino basics, digital outputs, and timing functions.


# 🚦 Arduino Traffic Light System

This project simulates a **traffic light** using an **Arduino Uno** and three LEDs (Red, Yellow, Green). It demonstrates basic digital output control and timing delays, making it ideal for beginners learning Arduino programming and electronics.

## 🔧 Components Required
- Arduino Uno  
- Red LED  
- Yellow LED  
- Green LED  
- 3 × 220Ω resistors  
- Jumper wires  
- Breadboard  

## 🚦 How It Works
The Arduino turns on each LED in sequence to mimic real traffic lights:
1. **Red** – Stop  
2. **Green** – Go  
3. **Yellow** – Prepare to stop  

Each light stays on for a set time using `delay()`.

## 🛠️ Code Example
```cpp
int red = 8;
int yellow = 9;
int green = 10;

void setup() {
  pinMode(red, OUTPUT);
  pinMode(yellow, OUTPUT);
  pinMode(green, OUTPUT);
}

void loop() {
  digitalWrite(red, HIGH);
  delay(3000);

  digitalWrite(red, LOW);
  digitalWrite(green, HIGH);
  delay(3000);

  digitalWrite(green, LOW);
  digitalWrite(yellow, HIGH);
  delay(1000);

  digitalWrite(yellow, LOW);
}
