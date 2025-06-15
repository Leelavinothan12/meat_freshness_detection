
# 🥩 Meat Freshness and Formalin Contamination Detection System

This project is a smart, AI-powered system designed to detect **meat freshness** and **formalin (CH2O) contamination** in meat and fish. It utilizes a combination of **gas sensors**, **formalin sensors**, **pH sensors**, and a **YOLOv8 deep learning model** deployed on a **Raspberry Pi 4**.

## 🚀 Features

- ✅ Detects if meat/fish is **fresh or spoiled**
- ✅ Detects **formalin contamination** using CH2O ZE-08 sensor
- ✅ pH-based freshness measurement
- ✅ Uses **YOLOv8 model** for meat freshness classification via image analysis
- ✅ Works offline on **Raspberry Pi 4B**
- ✅ Displays result on an LCD/GUI: **"Fresh"** or **"Spoiled"**
- ✅ Suitable for markets, food inspection units, and quality control labs

---

## 🧠 Technologies Used

| Component        | Details                              |
|------------------|--------------------------------------|
| 🧠 Model          | YOLOv8 (for visual spoilage detection) |
| 🤖 ML Algorithm  | Random Forest (for sensor fusion)     |
| 🧪 Sensors        | pH sensor, CH2O ZE-08, MQ135, MQ4, MQ137, H2S-01, TGS2602 |
| 💻 Device        | Raspberry Pi 4B                       |
| 🔌 Communication | Serial UART, GPIO                     |
| 📦 Backend       | Python (with OpenCV, scikit-learn)    |

---

## 📊 Architecture Overview

1. **Image-based YOLOv8 model** classifies meat as fresh/spoiled.
2. **Sensors** detect gases (ammonia, VOCs, hydrogen sulfide, methane) and formalin.
3. **Random Forest model** processes sensor values for spoilage prediction.
4. A **combined decision logic** shows the final result. If **any model/sensor detects spoilage**, the result is **"SPOILED"**.

---

## 🔍 Sensor Details

| Sensor           | Purpose                          |
|------------------|----------------------------------|
| CH2O ZE-08       | Formalin detection               |
| MQ135            | VOCs, Ammonia detection          |
| MQ4              | Methane detection                |
| MQ137            | Ammonia detection                |
| H2S-01           | Hydrogen sulfide detection       |
| TGS2602          | VOCs and spoiled meat gases      |
| pH Sensor        | Meat acidity level               |

---

## 🛠️ Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/meat-freshness-detector.git
   cd meat-freshness-detector
