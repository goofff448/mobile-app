# 🎮☢️ THE SCHRÖDINGER PROTOCOL

> **A Gamified Radiobiology Simulation Mobile App**
> 
> *Experience quantum superposition meets radiation physics in this immersive tactical radiation scanner simulation.*

[![GitHub Release](https://img.shields.io/github/v/release/goofff448/mobile-app?style=flat-square)](https://github.com/goofff448/mobile-app/releases)
[![GitHub License](https://img.shields.io/github/license/goofff448/mobile-app?style=flat-square)](LICENSE)
[![React Native](https://img.shields.io/badge/React%20Native-0.81.5-blue?style=flat-square&logo=react)](https://reactnative.dev/)
[![Expo](https://img.shields.io/badge/Expo-54.0.34-blue?style=flat-square&logo=expo)](https://expo.dev/)
[![Python](https://img.shields.io/badge/Python-3.9+-green?style=flat-square&logo=python)](https://www.python.org/)

---

## 📖 Overview

**THE SCHRÖDINGER PROTOCOL** is an educational mobile game that simulates real-world radiobiology physics with scientific accuracy. Players configure radiation scenarios, seal them in a quantum chamber, and observe the outcome—bringing Schrödinger's cat thought experiment to life.

Whether you're a physics student, nuclear medicine professional, or science enthusiast, this app provides an immersive way to understand:
- ⚛️ **Radiation types and properties**
- 🛡️ **Shielding effectiveness**
- 🏥 **Acute Radiation Syndrome (ARS)**
- 📊 **Dose-response relationships**

---

## ✨ Features

### 📱 Three-Screen Immersive Experience

#### **Screen 1: Scanner Dashboard**
- 🎚️ **Interactive Controls:**
  - Radiation dose slider (0-10 Sv)
  - 4 radiation types: Alpha, Beta, Gamma, Neutron
  - 3 shielding materials: Lead, Concrete, Water
  - Adjustable shielding thickness (0-50 cm)
- 📊 **Real-time Gauge:**
  - Live survival probability percentage
  - Dynamic lethality indicator
  - Threat level color indicator (Green → Yellow → Orange → Red → Black)
- 🎨 **Military Tactical UI** with HUD-style elements

#### **Screen 2: Quantum Chamber (Superposition)**
- 🌀 Immersive pulsing chamber animation with rotating rings
- 📳 Geiger counter haptic feedback simulation (accelerating vibrations)
- ⚛️ Real-time calculation progress display
- 🔮 Dramatic wavefunction collapse simulation

#### **Screen 3: Diagnostic Readout**
- 🏥 Complete medical diagnosis with ARS syndrome classification
- 📋 Detailed clinical symptoms in terminal-style display
- ☢️ Radiation analysis with penetration and ionization data
- 🛡️ Shielding effectiveness breakdown
- 💊 Treatment recommendations and medical codes

---

## 🧪 Scientific Accuracy

### Physics Models
- **Shielding Attenuation:** Half-Value Layer (HVL) exponential decay
- **Survival Probability:** Logistic curve with LD₅₀ = 4.5 Sv
- **Medical Classification:** WHO Acute Radiation Syndrome standards

### Validation Results
✅ LD₅₀ curve accuracy: 4.5 Sv = 50% survival
✅ Alpha shielding: 100% blocked by 1cm lead
✅ Gamma shielding: 99.9% blocked by 10cm lead
✅ Neutron + water: 99% blocked by 20cm (optimal combo)
✅ 8/8 backend physics tests passed

---

## 🚀 Quick Start

### Prerequisites
- Node.js 16+ and npm/yarn
- Python 3.9+ (for backend development)
- Expo CLI: `npm install -g expo-cli`

### Installation

**Clone the repository:**
```bash
git clone https://github.com/goofff448/mobile-app.git
cd mobile-app
```

**Frontend Setup:**
```bash
cd frontend
yarn install
# or: npm install
```

**Backend Setup:**
```bash
cd backend
pip install -r requirements.txt
```

### Running the App

**Development Mode (Frontend):**
```bash
cd frontend
expo start
```
Then:
- 📱 Scan QR code with **Expo Go** app (iOS/Android)
- 🌐 Press `w` for **web preview**
- 🍎 Press `i` for **iOS simulator**
- 🤖 Press `a` for **Android emulator**

**Development Mode (Backend):**
```bash
cd backend
uvicorn main:app --reload --host 0.0.0.0 --port 8001
```
API docs available at: `http://localhost:8001/api/docs`

---

## ⚙️ Environment Variables

**Frontend (.env):**
```env
EXPO_PUBLIC_BACKEND_URL=http://localhost:8001
EXPO_TUNNEL_SUBDOMAIN=dose-measure
```

**Backend (.env):**
```env
MONGODB_URI=mongodb://localhost:27017
DATABASE_NAME=radiation_db
LOG_LEVEL=INFO
```

---

## 🔧 Technical Stack

### Frontend
- **Framework:** React Native + Expo v54
- **Navigation:** Expo Router (file-based)
- **UI Libraries:**
  - `expo-linear-gradient` - Tactical gradients
  - `@react-native-community/slider` - Precision controls
  - `expo-haptics` - Vibration feedback
  - `react-native-reanimated` - Smooth animations
- **Language:** TypeScript

### Backend
- **Framework:** FastAPI (Python)
- **Database:** MongoDB
- **Physics Engine:** Custom radiobiology calculations
- **Validation:** Pydantic v2
- **API:** RESTful with auto-documentation

### API Endpoints
```
GET  /api/health                 - Engine health check
GET  /api/radiation-types        - Available radiation types
GET  /api/shielding-materials    - Available shielding materials
POST /api/calculate              - Calculate radiation scenario
GET  /api/experiments            - Retrieve experiment history
```

---

## 📚 Radiation Types Reference

| Type | Symbol | Penetration | Ionization | Best Shielding |
|------|--------|------------|-----------|-----------------|
| **Alpha** | α | LOW | EXTREME | Paper/Skin |
| **Beta** | β | MEDIUM | HIGH | Aluminum |
| **Gamma** | γ | HIGH | MODERATE | Lead (1.0 cm HVL) |
| **Neutron** | n | EXTREME | HIGH | Water (3.0 cm HVL) |

---

## 🏥 ARS Syndrome Classification

| Dose Range | Syndrome | Threat | Survival Rate |
|-----------|----------|--------|----------------|
| < 1 Gy | Subclinical | 🟢 GREEN | 100% |
| 1-2 Gy | Mild ARS | 🟡 YELLOW | 90-100% |
| 2-6 Gy | Hematopoietic | 🟠 ORANGE | 20-80% |
| 6-10 Gy | Gastrointestinal | 🔴 RED | 5-20% |
| > 10 Gy | Neurovascular | ⚫ BLACK | 0% |

---

## 📖 How to Use

### Step 1: Configure Scenario
1. Adjust **Radiation Dose** slider
2. Select **Radiation Type**
3. Choose **Shielding Material**
4. Set **Shielding Thickness**
5. Watch **real-time survival gauge**

### Step 2: Observe Quantum Superposition
1. Tap **"SEAL & INITIALIZE"**
2. Experience **pulsing chamber animation**
3. Feel **accelerating Geiger counter haptics**
4. Wait for **calculation to complete**

### Step 3: Review Diagnostic Results
1. See **ALIVE or DECEASED** outcome
2. Review **survival/lethality percentages**
3. Read **medical diagnosis** and symptoms
4. Check **radiation analysis**
5. Tap **"NEW EXPERIMENT"** to try again

---

## 🎨 Design Philosophy

### Military Tactical Theme
- **Dark aesthetic** with red/orange/green accents
- **Monospace fonts** for terminal authenticity
- **HUD-style elements** for immersion
- **Color-coded threat levels** for quick recognition

### Mobile-First UX
- ✅ Touch-optimized controls (44pt minimum)
- ✅ Safe area handling for notches
- ✅ Responsive layouts for all screen sizes
- ✅ Platform-specific haptics (iOS/Android)
- ✅ Smooth 60fps animations

---

## 📊 Project Structure

```
mobile-app/
├── frontend/                    # React Native + Expo app
│   ├── app/
│   │   ├── index.tsx           # Scanner Dashboard
│   │   ├── superposition.tsx   # Quantum Chamber
│   │   └── diagnostic.tsx      # Diagnostic Readout
│   ├── package.json
│   └── .env
├── backend/                     # FastAPI server
│   ├── main.py                 # API endpoints
│   ├── radiobiology_engine.py  # Physics calculations
│   ├── database.py             # MongoDB models
│   ├── requirements.txt
│   └── .env
├── RELEASE_NOTES.md            # v1.0.0 release details
├── README.md                   # This file
└── package.json               # Root workspace config
```

---

## 🧬 Educational Value

### Learning Outcomes
- Understand different radiation types and their properties
- Learn shielding effectiveness and Half-Value Layers
- Comprehend Acute Radiation Syndrome (ARS) classification
- Grasp dose-response relationships in radiobiology
- Appreciate nuclear safety principles

### Target Audience
- 🎓 Physics and medical students
- 👨‍⚕️ Nuclear medicine professionals
- 🚒 Emergency response personnel
- 🔬 Science educators
- 📚 Lifelong learners

---

## 📝 Data Sources

- **LD₅₀ values:** Hiroshima/Nagasaki survivor studies
- **Half-Value Layers:** NIST radiation safety handbooks
- **ARS symptoms:** IAEA Emergency Response guidance
- **Medical classifications:** WHO radiation protocols

---

## ⚠️ Disclaimer

**This is an educational simulation** for learning purposes only. All calculations are based on peer-reviewed radiobiology literature and are scientifically accurate.

**This app should NOT be used for:**
- ❌ Actual radiation safety planning
- ❌ Medical diagnosis or treatment
- ❌ Professional nuclear safety decisions

**Always consult qualified radiation safety professionals and medical experts for real-world applications.**

---

## 🔮 Future Roadmap

### v1.1.0 (Planned)
- Firebase cloud synchronization
- User authentication system
- Experiment history dashboard
- Achievement/badge system

### v1.2.0 (Planned)
- Educational tutorial mode
- Real-world historical scenarios
- Advanced statistics dashboard
- User profile system

### v2.0.0 (Planned)
- Time-dependent dose calculations
- Organ-specific radiation sensitivity
- Secondary radiation effects
- Environmental factors (temperature, humidity)

---

## 📞 Support & Feedback

- 📋 **Issues:** [GitHub Issues](https://github.com/goofff448/mobile-app/issues)
- 💬 **Discussions:** [GitHub Discussions](https://github.com/goofff448/mobile-app/discussions)
- 📧 **Email:** sanchit4apr@gmail.com

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Hiroshima/Nagasaki survivor studies for LD₅₀ data
- NIST for radiation safety reference materials
- IAEA for emergency response protocols
- WHO for radiation safety standards
- Expo and React Native communities
- FastAPI documentation

---

## 🎯 Key Stats

- ⚛️ **4 radiation types** with accurate physics
- 🛡️ **3 shielding materials** with real HVL data
- 📊 **Medical accuracy** based on WHO standards
- ✅ **8/8 backend tests** passed
- 📱 **Cross-platform** (iOS, Android, Web)
- 🎮 **3 immersive screens** with animations

---

## 🚀 Get Started Now

**Try it today:**
1. Clone: `git clone https://github.com/goofff448/mobile-app.git`
2. Install: `cd frontend && yarn install`
3. Run: `expo start`
4. Scan with Expo Go app

---

<div align="center">

**Built with scientific rigor and mobile-first design principles.**

**Experience the quantum mechanics of life and death. ☢️⚛️**

[⬆ back to top](#-the-schrödinger-protocol)

</div>
