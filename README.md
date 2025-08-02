# 🏋️‍♂️ FitSplit: Smart Gym Logger and Workout Recommendation System

FitSplit is a smart gym attendance and personalized workout recommendation system that combines RFID/NFC technology and Machine Learning to streamline user entry logging and deliver data-driven workout planning.

<div align="center">
  <img src="https://img.shields.io/badge/Platform-Arduino-blue" />
  <img src="https://img.shields.io/badge/Machine%20Learning-KMeans-yellow" />
  <img src="https://img.shields.io/badge/Language-Python%20%7C%20C++-critical" />
  <img src="https://img.shields.io/badge/Hardware-RFID/NFC-orange" />
</div>

---

## 🔍 Problem Statement

Manual gym check-ins are inefficient and don't leverage data for user insights. FitSplit automates entry logging using RFID/NFC and clusters gym-goers based on attendance behavior to recommend optimal workout plans.

---

## 🎯 Project Objectives

- ✅ Automatically log user entries via RFID/NFC
- ✅ Track attendance patterns
- ✅ Recommend personalized workout splits using ML (K-Means clustering)
- ✅ Identify user types: Beginner, Intermediate, Advanced
- ✅ Encourage consistency through gamified features

---

## 🧠 How It Works

### 1. **Hardware Setup**
- **RC522 RFID Module**
- **Arduino UNO**
- **RFID/NFC Tags**

Each gym-goer taps their RFID card to log entry. The UID is sent to the PC via Serial.

### 2. **Data Logging (Python)**
The Python script listens to the serial port and logs:
- UID
- Timestamp
- Day, Week, Month

Stored in `RFID_logs.csv`.

### 3. **Machine Learning Module**
- Parses attendance patterns from CSV
- Extracts features like:
  - Visit frequency
  - Consistency (gap std deviation)
  - Time-of-day preference
  - Day-of-week behavior
- Uses **K-Means Clustering** to categorize users
- Stores trained model for future predictions

---

## 🧰 Technologies Used

| Domain | Tools & Libraries |
|--------|-------------------|
| Hardware | Arduino UNO, RC522 RFID |
| Programming | C++, Python |
| ML & Data Processing | Pandas, Scikit-learn, KMeans, Joblib |
| Visualization & Logging | CSV, Serial Monitor |

---

## 📸 Circuit Connections

| RC522 Pin | Arduino Pin |
|-----------|-------------|
| VCC       | 3.3V        |
| GND       | GND         |
| RST       | 9           |
| MISO      | 12          |
| MOSI      | 11          |
| SCK       | 13          |
| SDA (SS)  | 10          |

---

## 🚀 Use Cases

- 🛂 **Contactless Check-In**: No manual logging
- 🧠 **Smart Recommendations**: Suggest best time/day to work out
- 🧩 **User Classification**: Tailored workout plans
- 🕹️ **Gamification**: Badges, streaks, milestones
- 📊 **Manager Insights**: Detect churn, plan staffing

---

## 🔮 Future Scope

- 🤖 Deep Learning for user goals (fat loss, hypertrophy)
- 📱 Mobile App with real-time analytics
- 🏆 Social Features: Leaderboards, group workouts
- 🏋️ Integration with smart equipment
- 🌐 Multi-branch gym support

---


> The system successfully automates gym attendance and delivers meaningful workout insights based on real usage patterns. It is scalable, cost-effective, and a stepping stone towards AI-powered fitness personalization.
