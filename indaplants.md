
---

### **indaplants.md**

```markdown
---
layout: page
title: "IndaPlants Experiment – Autonomous Holonomic Plant‑Care Robots"
permalink: /indaplants/
---

> **Capstone Mechatronics Project – 2023**  
> Co‑authors: S. Sabaroche, A. Malik, Y. Fernandez  
> 24‑page Design Report & Test Log available on request.

## Project Goal
Demonstrate that a **cooperative swarm** of low‑cost holonomic robots can monitor and service houseplants better than a single caretaker by mapping, sharing, and scheduling visits to **light, water, and humidity** resources in real time.

## Hardware Stack
| Sub‑assembly | Components | Notes |
|--------------|-----------|-------|
| Drive chassis | Triangular aluminium deck; 3 × 100 mm omni‑wheels; BLDC motors (11 kV, 24 V); AMT102‑V encoders | 0.50 m/s top speed; inverse‑kinematics matrix converts **vₓ, vᵧ, ω** to wheel RPMs |
| Power & PCBs | 24 V 6‑cell Li‑ion 5 Ah; 5 V 6 A buck; 12 V rail | ~2 h runtime incl. pump |
| Sensors | Pixy CMU‑cam 5; HC‑SR04 sonar ring; Grove sunlight; DHT11 RH/Temp; capacitive soil‑moisture | Beacon recognition, obstacle ranging, irrigation trigger |
| Control | Arduino Mega 2560 @ 16 MHz; TB6612FNG drivers | PID @ 50 Hz; Kp 1.4, Ki 0.05, Kd 0.12 |
| Comms | XBee S2 ZigBee (API mode) | 40‑byte status frames every 200 ms |
| Actuation | 12 V mini‑peristaltic pump (300 mL reservoir) | 5–30 mL/min drip |

## Software Architecture
```mermaid
graph TD
A(Main loop 20 Hz) --> B(Sensor fusion / EKF)
B --> C(Global grid map)
C --> D{Need resource?}
D -- yes --> E(A* path‑planning)
E --> F(Motion command queue)
F --> G(PID velocity controller)
D -- no --> H(Health telemetry / idle)
