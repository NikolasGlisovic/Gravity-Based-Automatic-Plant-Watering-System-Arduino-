# 🌱 Gravity-Based Automatic Plant Watering System (Arduino)

This project is a **simple, reliable, and energy-efficient automatic watering system** for houseplants or balcony plants — **without using a water pump and without using soil moisture sensors**.

The system uses:
- a arduino nano for controlling everything,
- a real-time clock (RTC) for precise timing,
- gravity as the water source,
- and a servo motor to mechanically open and close a silicone tube.

A single button press starts the automatic watering cycle, which then repeats autonomously every 7 days.

---

## 📷 Images

<table>
  <tr>
    <td align="center">
      <img src="Images/System_overview.jpg" width="200"/><br/>
      <b>System overview</b>
    </td>
    <td align="center">
      <img src="Images/Mounted_water_tank.jpg" width="200"/><br/>
      <b>Mounted water tank</b>
    </td>
    <td align="center">
      <img src="Images/Electronics_enclosure.jpg" width="200"/><br/>
      <b>Electronics enclosure</b>
    </td>
    <td align="center">
      <img src="Images/Tube_bending_mechanism.jpg" width="200"/><br/>
      <b>Tube bending mechanism</b>
    </td>
  </tr>
</table>

---

## ✨ Features

- No water pump → silent, low power, and reliable
- No moisture sensor → simple and robust logic, no misplacement of any sensors
- Gravity-fed watering from an elevated water tank
- RTC-based timing (independent from Arduino uptime)
- Manual start button for the watering cycle
- Fully 3D-printable mechanical parts

---

## 🧠 How It Works

1. A water tank is mounted above the plant using a French cleat.
2. Water flows from the tank through a silicone tube into the plant by gravity.
3. A servo motor bends the silicone tube to block or allow water flow.
4. A real-time clock module (DS1307) provides accurate timing.
5. The Arduino controls the servo based on time intervals.
6. A button press starts the automatic watering loop.

### Watering Logic

- Press button → start automatic loop
- Servo opens the tube for **10 seconds** (watering around 175 ml)
- Servo closes the tube for **7 days**
- Cycle repeats automatically

---

## 🔌 Hardware Components

| Component | Description |
|----------|-------------|
| Arduino Nano | Main microcontroller |
| Elegoo RTC Module (DS1307) | Time keeping |
| Micro Servo Motor | Controls tube bending |
| 4 mm inner diameter, 6mm outside diameter Silicone Tube | Water transport |
| Push Button | Manual cycle start |
| 5V Power Supply | Servo power |

---

## 🧩 3D Printed Parts

All mechanical parts are designed to be 3D printable.

### 1. Water Tank Assembly
- Water tank container
- Removable lid
- French cleat mounting system (made for 19mm thick wood, cut in a 45° angle) 
- Hose connector (5 mm tube interface for 4 mm silicone hose)

The silicone tube is pushed onto a 5 mm pipe through which the water flows.

---

### 2. Electronics Housing & Pot Mount

- Enclosure for:
  - Arduino Nano
  - RTC module
  - wiring
- Opening for the start button and cables
- holder to attach the electronics housing to the plant pot. It needs to be glued on.

---

### 3. Water Flow Control Mechanism

This consists of two printed parts:

#### a) Tube & Servo Holder
- Rigidly positions the servo motor and silicone tube relative to each other

#### b) Servo Tube Bender
- Attaches to the servo
- Presses and bends the silicone tube when rotated
- Fully blocks water flow when bent
- Releases tube when rotated back

This allows the servo to act as a mechanical valve without direct contact with water.

---

## 🛠 Wiring

| Arduino Nano Pin | Connected To |
|------------------|-------------|
| D9 | Servo signal |
| D7 | Push button |
| A4 | RTC SDA |
| A5 | RTC SCL |
| 5V | RTC VCC |
| GND | RTC GND and button |

---

## 💻 Software

### Required Libraries

- RTClib by Adafruit
- Servo (included with Arduino IDE)
- Wire (included)

---

## 🚀 Setup

1. Upload the Arduino sketch.
2. Insert CR2032 battery into the RTC module.
3. Set the water tank above the plant.
4. Fill the tank with water.
5. Press the start button once.

---

## 📄 License

Open-source — feel free to modify, improve, and share.

---

## 🙌 Credits

Designed and built by Nikolas Glisovic.

