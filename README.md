# Servo Motor Position Control using HMI & PLC (GT Designer3 + Ladder Logic)

This project demonstrates the **servo motor position control** using an HMI designed in **GT Designer3 (GOT2000)** and programmed using **MELSOFT Ladder Logic**. The system is capable of operating in **Home Mode**, **Jog Mode**, and **Position Mode**, and uses a **MR-JE-40AS servo motor**.

---

## 📷 HMI Screens

### ➤ GT Simulator Runtime Screen

![GT Simulator Screen](images/HMI_Simulator.png)

> This screen shows the real-time simulation of the servo motor system with active position control and mode selection.

---

### ➤ GT Designer HMI Design Screen

![GT Designer HMI Screen](images/HMI_Design_Screen.png)

> HMI screen developed using GT Designer3 for Mitsubishi's GOT2000 series HMI. This layout allows mode switching, emergency handling, and position selection.

---

## ⚙️ System Overview

- **HMI Tool:** GT Designer3 (GOT2000 Series)
- **PLC Tool:** MELSOFT GX Works / Ladder Logic
- **Motor:** Servo Motor
- **Modes:** 
  - Home Mode
  - Jog Mode
  - Position Mode
- **Simulation Tool:** GT Simulator3

---

## 🧠 Mode Descriptions

### 🔹 Home Mode
- **Buttons:** Enable & Start
- **Function:** Returns servo motor to initial reference/home position.

### 🔹 Jog Mode
- **Buttons:** Enable, Jog Forward, Jog Reverse
- **Function:** Allows manual fine-tuned movement.

### 🔹 Position Mode
- **Buttons:** Enable, Position 1/2/3 Select
- **Function:** Moves motor to predefined positions with visual indication.

---

## 🪜 PLC Ladder Logic (GX Works)

- Implements all three modes using internal memory bits (`M0`, `M1`, `M2`, etc.)
- Controls:
  - Forward and Reverse Moves (`Y1`, `Y2`)
  - Mode Enable Flags
  - Safety Interlocks (e.g. Emergency Stop using `X103`)
- Data Registers:
  - `D0`: Actual Position
  - `D1`, `D2`, etc.: Set Positions
- Uses `MOV`, comparison (`>`, `<`), and memory-based control logic.

You can view the full logic inside [`PLC_Ladder_Logic.html`](PLC%20Lader%20Logic%20Programming.html)

---

## 📁 Project Files

| File | Description |
|------|-------------|
| `HMI_Simulator.png` | Screenshot of the GT Simulator running the project |
| `HMI_Design_Screen.png` | GT Designer3 screen of the HMI design |
| `PLC_Ladder_Logic.html` | Ladder Logic logic used to program the PLC (Mitsubishi) |
| `README.md` | Project documentation |

---

## 🚀 How to Run

1. Open `.GTX` project in **GT Designer3**.
2. Load `.html` ladder logic into **GX Works2/3**.
3. Connect to hardware or simulate using **GT Simulator3**.
4. Test all modes via the HMI panel.

---

## 📄 License

This project is for educational/demo purposes only.


