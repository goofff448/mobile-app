# Release Notes - v1.0.0

## 🎮 The Schrödinger Protocol v1.0.0 - Initial Release

**Release Date:** May 24, 2026

A gamified radiobiology simulation mobile app that brings quantum mechanics and radiation physics to life. Experience the intersection of scientific accuracy and immersive mobile gaming.

---

## ✨ Features

### 📱 Three-Screen Mobile Experience

#### **Screen 1: Scanner Dashboard**
- 🎚️ Interactive radiation dose slider (0-10 Sv)
- 4 radiation types: Alpha (α), Beta (β), Gamma (γ), Neutron (n)
- 3 shielding materials: Lead, Concrete, Water
- Adjustable shielding thickness (0-50 cm)
- Real-time survival probability gauge
- Dynamic lethality percentage display
- Threat level indicator (Green → Yellow → Orange → Red → Black)

#### **Screen 2: Quantum Chamber (Superposition)**
- Immersive pulsing radiation chamber animation
- Rotating rings with glow effects
- Geiger counter haptic feedback simulation
- Real-time calculation progress display
- Dramatic wavefunction collapse animation
- Parameter verification before measurement

#### **Screen 3: Diagnostic Readout**
- Complete medical diagnosis with ARS syndrome classification
- Survival/lethality statistics
- Clinical symptoms in terminal-style display
- Radiation properties and characteristics
- Shielding effectiveness analysis
- Material breakdown and penetration data
- Medical codes and treatment recommendations

### 🎨 Military Tactical UI
- Dark theme with professional HUD-style elements
- Color-coded threat warnings (Red, Orange, Yellow, Green)
- Monospace terminal fonts for authenticity
- Smooth animations with haptic feedback
- Fully responsive mobile design

### ⚛️ Scientific Accuracy
- **Physics Models:** Half-Value Layer attenuation, exponential decay
- **Medical Accuracy:** Acute Radiation Syndrome (ARS) classification per WHO standards
- **Dose-Response:** Logistic curve for survival probability
- **LD₅₀:** 4.5 Sv based on Hiroshima/Nagasaki survivor data

### 📳 Platform Support
- ✅ iOS (via Expo Go or compiled app)
- ✅ Android (via Expo Go or compiled app)
- ✅ Web (React Native Web)
- ✅ Haptic feedback (iOS/Android native)

---

## 🧪 Tested & Validated

### Backend Physics Engine
```
✅ 8/8 Test Cases Passed
✅ Health check endpoint operational
✅ Radiation types properly configured
✅ Shielding materials loaded correctly
✅ Survival scenario calculations accurate
✅ Lethal scenario calculations accurate
✅ Edge case handling (no shielding)
✅ Database persistence verified
✅ Input validation functioning
```

### Physics Validation Results
- ✅ LD₅₀ curve: 4.5 Sv = 50% survival probability
- ✅ Alpha shielding: 100% blocked by 1cm lead
- ✅ Gamma shielding: 99.9% blocked by 10cm lead
- ✅ Neutron + water: 99% blocked by 20cm (optimal combo)
- ✅ No shielding: 0% effectiveness (full dose absorbed)

---

## 📦 Technical Stack

### Frontend
- **Framework:** Expo + React Native v0.81.5
- **Navigation:** Expo Router (file-based routing)
- **UI Libraries:**
  - `expo-linear-gradient` - Tactical gradients
  - `@react-native-community/slider` - Precision controls
  - `expo-haptics` - Vibration feedback
  - `react-native-reanimated` - Smooth animations
- **TypeScript:** Full type safety

### Backend
- **Framework:** FastAPI (Python)
- **Database:** MongoDB
- **Physics Engine:** Custom radiobiology calculations
- **API:** RESTful endpoints with Pydantic v2 validation

### API Endpoints
```
GET  /api/health                 - Engine health check
GET  /api/radiation-types        - Available radiation types
GET  /api/shielding-materials    - Available shielding materials
POST /api/calculate              - Calculate radiation scenario
GET  /api/experiments            - Retrieve experiment history
```

---

## 🚀 Getting Started

### Prerequisites
- Node.js 16+ and npm/yarn
- Python 3.9+ (for backend development)
- Expo CLI: `npm install -g expo-cli`

### Installation

#### Frontend Setup
```bash
cd frontend
yarn install
# or npm install
```

#### Backend Setup
```bash
cd backend
pip install -r requirements.txt
```

### Running the App

#### Development Mode (Frontend)
```bash
cd frontend
expo start
# Scan QR code with Expo Go app (iOS/Android)
# Or press 'w' for web preview
```

#### Development Mode (Backend)
```bash
cd backend
uvicorn main:app --reload --host 0.0.0.0 --port 8001
```

### Environment Variables

**Frontend (.env):**
```
EXPO_TUNNEL_SUBDOMAIN=dose-measure
EXPO_PUBLIC_BACKEND_URL=http://localhost:8001
EXPO_PACKAGER_HOSTNAME=http://localhost:19000
```

**Backend (.env):**
```
MONGODB_URI=mongodb://localhost:27017
DATABASE_NAME=radiation_db
LOG_LEVEL=INFO
```

---

## 📚 Educational Value

### Learning Outcomes
1. **Radiation Physics:** Types, properties, and attenuation
2. **Radiobiology:** ARS syndromes and dose-response relationships
3. **Nuclear Safety:** Shielding effectiveness and protection principles
4. **Medical Science:** Acute radiation effects on human physiology

### Target Audience
- Physics students and educators
- Nuclear medicine professionals
- Emergency response personnel
- Science enthusiasts
- General education

---

## 🔬 Radiation Type Reference

| Type | Symbol | Penetration | Ionization | Best Shielding |
|------|--------|------------|-----------|-----------------|
| Alpha | α | LOW | EXTREME | Paper/Skin |
| Beta | β | MEDIUM | HIGH | Aluminum |
| Gamma | γ | HIGH | MODERATE | Lead (1.0 cm HVL) |
| Neutron | n | EXTREME | HIGH | Water (3.0 cm HVL) |

---

## 📊 ARS Syndrome Classification

| Dose Range | Syndrome | Threat Level | Survival |
|-----------|----------|--------------|----------|
| < 1 Gy | Subclinical | 🟢 GREEN | 100% |
| 1-2 Gy | Mild ARS | 🟡 YELLOW | 90-100% |
| 2-6 Gy | Hematopoietic | 🟠 ORANGE | 20-80% |
| 6-10 Gy | Gastrointestinal | 🔴 RED | 5-20% |
| > 10 Gy | Neurovascular | ⚫ BLACK | 0% |

---

## 🎯 Key Improvements in v1.0.0

- ✅ Complete 3-screen mobile experience
- ✅ Real-time physics calculations
- ✅ Scientifically validated models
- ✅ Military tactical UI design
- ✅ Haptic feedback integration
- ✅ Cross-platform support
- ✅ MongoDB data persistence
- ✅ Comprehensive error handling

---

## 📝 Known Limitations

- Haptic feedback limited to iOS/Android (not available on web)
- Backend requires local MongoDB instance
- Some animations may impact performance on older devices
- Web version uses simulated haptics

---

## 🔮 Future Roadmap

### Planned for v1.1.0
- Firebase cloud synchronization
- User authentication system
- Experiment history dashboard
- Achievement/badge system

### Planned for v1.2.0
- Educational tutorial mode
- Real-world historical scenarios
- Advanced statistics dashboard
- User profile system

### Planned for v2.0.0
- Time-dependent dose calculations
- Organ-specific radiation sensitivity
- Secondary radiation effects
- Temperature/humidity environmental factors

---

## 📖 Documentation

- **[README.md](./README.md)** - Complete feature documentation
- **[SETUP.md](./SETUP.md)** - Detailed setup instructions
- **API Documentation** - Available at `/api/docs` (Swagger UI)

---

## ⚠️ Disclaimer

**This is an educational simulation** for learning purposes only. All calculations are based on peer-reviewed radiobiology literature and are scientifically accurate. 

**This app should NOT be used for:**
- Actual radiation safety planning
- Medical diagnosis or treatment
- Professional nuclear safety decisions

Always consult qualified radiation safety professionals and medical experts for real-world applications.

---

## 🙏 Acknowledgments

- Hiroshima/Nagasaki survivor studies for LD₅₀ data
- NIST radiation safety handbooks for HVL values
- IAEA emergency response guidance for ARS classification
- WHO radiation safety protocols
- Expo and React Native communities

---

## 📞 Support & Feedback

For issues, questions, or suggestions:
1. Check the [GitHub Issues](https://github.com/goofff448/mobile-app/issues)
2. Review the documentation
3. Contact via GitHub Discussions

---

## 📄 License

This project is provided for educational purposes. See LICENSE file for details.

---

**Built with scientific rigor and mobile-first design principles.**

**Experience the quantum mechanics of life and death. ☢️⚛️**

---

**v1.0.0 - May 24, 2026**
