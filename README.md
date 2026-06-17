
<div align="center">

# Rotary Kiln Control System

### Industrial PLC Automation Project

![PLC](https://img.shields.io/badge/PLC-Omron%20CJ2M-blue?style=for-the-badge)
![Software](https://img.shields.io/badge/CX--Programmer-Ladder%20Logic-green?style=for-the-badge)
![IEC61131-3](https://img.shields.io/badge/IEC%2061131--3-Compliant-orange?style=for-the-badge)
![State Machine](https://img.shields.io/badge/Architecture-State%20Machine-red?style=for-the-badge)

---

### 🔥 Burner Management • ⚙️ Process Control • 🏭 Industrial Automation

</div>

---

## 📖 Project Overview

This project implements a complete **Rotary Kiln Control System** using an **Omron CJ2M PLC** programmed in **CX-Programmer**.

The control philosophy is based on a robust **State Machine Architecture** combined with **PID Temperature Control** to ensure safe startup, combustion management, process stability, and controlled shutdown.

---

## 🏭 System Architecture

```text
                    ┌────────────────────┐
                    │      Operator HMI   │
                    └─────────┬──────────┘
                              │
                              ▼
                    ┌────────────────────┐
                    │     Omron CJ2M     │
                    │        PLC         │
                    └─────────┬──────────┘
                              │
      ┌─────────────┬─────────┼─────────┬─────────────┐
      ▼             ▼         ▼         ▼             ▼

 ┌────────┐   ┌────────┐ ┌────────┐ ┌────────┐ ┌────────┐
 │ ID Fan │   │ FD Fan │ │ Burner │ │ Sensors│ │Conveyor│
 └────────┘   └────────┘ └────────┘ └────────┘ └────────┘
```

---

## 🔄 State Machine

```text
┌────────────┐
│   IDLE     │
└─────┬──────┘
      ▼
┌────────────┐
│ PRESTART   │
└─────┬──────┘
      ▼
┌────────────┐
│   PURGE    │
└─────┬──────┘
      ▼
┌────────────┐
│ IGNITION   │
└─────┬──────┘
      ▼
┌────────────┐
│ FLAME VER. │
└─────┬──────┘
      ▼
┌────────────┐
│  WARMUP    │
└─────┬──────┘
      ▼
┌────────────┐
│PRODUCTION  │
└─────┬──────┘
      ▼
┌────────────┐
│ SHUTDOWN   │
└────────────┘
```

---

## ✨ Key Features

### 🔥 Burner Management

- [x] Automatic Purge Sequence
- [x] Ignition Control
- [x] Flame Verification
- [x] Flame Failure Protection
- [x] Fuel Valve Interlocking

### ⚙️ Process Control

- [x] PID Temperature Control
- [x] 900°C Setpoint Control
- [x] Kiln Temperature Monitoring
- [x] Pressure Monitoring
- [x] Production Mode Control

### 🛡️ Safety Functions

- [x] Emergency Stop
- [x] Motor Overload Protection
- [x] High Temperature Shutdown
- [x] Low Pressure Protection
- [x] Controlled Shutdown Sequence

---

## 🚀 Startup Sequence

```text
START
  │
  ▼
Permissive Check
  │
  ▼
Start ID Fan
  │
  ▼
Start FD Fan
  │
  ▼
Start Kiln Drive
  │
  ▼
5 Minute Purge
  │
  ▼
Open Fuel Valve
  │
  ▼
Ignition
  │
  ▼
Flame Verification
  │
  ▼
Warmup
  │
  ▼
Production
```

---

## 🚨 Alarm Matrix

| Alarm | Action |
|--------|---------|
| 🔥 High Temperature | Emergency Stop |
| 💨 Low Pressure | Fault State |
| 🔥 Flame Failure | Fuel Shutdown |
| ⚙️ Motor Overload | Fault State |
| 🚨 E-Stop | Immediate Shutdown |
| 📡 Sensor Failure | Fault State |

---

## 📸 Project Screenshots

### Symbol Table


<img width="942" height="880" alt="image" src="https://github.com/user-attachments/assets/00b1f8e6-fbf8-45c9-a0d7-81f315c80fe0" />

---

## 🧪 Testing

✅ State Machine Verification

✅ Purge Sequence Testing

✅ Ignition Testing

✅ Flame Failure Testing

✅ PID Control Verification

✅ Alarm Testing

✅ Emergency Stop Testing

✅ Shutdown Testing

---

## 🛠️ Development Environment

| Item | Description |
|--------|------------|
| PLC | Omron CJ2M |
| IDE | CX-Programmer |
| Language | Ladder Logic |
| Standard | IEC 61131-3 |
| Control Strategy | State Machine + PID |

---

```

