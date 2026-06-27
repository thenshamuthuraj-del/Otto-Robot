# Touch-Activated-Otto-Robot-with-Audio

# 🤖 Touch-Activated Otto Robot with Audio & Extra Servos

A playful robot built on the Otto DIY platform that reacts to **touch sensors** by dancing, moving its hands & head, and playing **audio tracks** through a JQ6500 MP3 module.

When idle, it performs a default dance loop until touched — turning this into an interactive demo great for:
- STEM workshops
- Tech fairs
- Robotics learning projects

---

## 🎛 **Features**
✅ Otto robot + extra servos for hands & head  
✅ Dual touch sensors trigger unique dances & audio  
✅ Default dance and music when untouched  
✅ Integrated JQ6500 MP3 audio playback  
✅ Debug logs over Serial Monitor

---

## ⚙ **Hardware Used**
- Arduino Nano / Uno / similar
- 4 servos for legs & feet (Otto standard)
- 3 extra servos: LeftHand, RightHand, Head
- JQ6500 MP3 module
- 2 touch sensors
- Passive buzzer (pin 10)
- Wires, power supply

---

## 🧰 **Libraries**
- [`Otto.h`](https://github.com/OttoDIY/OttoDIYLib)
- `Servo.h`
- `SoftwareSerial.h`

All installable via Arduino Library Manager or GitHub.

---

## 🔌 **Pin Configuration**
| Component        | Pin        |
|------------------|-----------:|
| LeftLeg servo    | 2         |
| RightLeg servo   | 3         |
| LeftFoot servo   | 4         |
| RightFoot servo  | 5         |
| LeftHand servo   | 6         |
| RightHand servo  | 7         |
| Head servo       | 8         |
| Touch Left       | A4        |
| Touch Right      | A5        |
| Buzzer & JQ6500 TX | 10      |
| JQ6500 RX        | 11        |

> ⚡ *Tip*: adjust pins if you use different boards.

---

## 🧠 **How it works**
1. Robot waits for touch:
   - Left sensor → plays left dance & audio track #1
   - Right sensor → plays right dance & audio track #2
2. If untouched → performs default dance loop with track #3
3. Audio controlled by sending commands over SoftwareSerial to JQ6500.
