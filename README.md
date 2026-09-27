# 🤝 Sahaayak (सहायक) — Cooperative Service Network

<p align="center">
  <img src="assets/images/logo.jpeg" alt="Sahaayak Logo" width="120" style="border-radius: 24px; box-shadow: 0 4px 20px rgba(0,0,0,0.15);" />
</p>

<p align="center">
  <strong>A Digital Operating System for Labour Cooperative Federations & Primary Societies</strong><br>
  <em>Transforming informal gig labour into democratic, verified, fair-wage cooperative enterprises.</em>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Flutter-3.47+-02569B?style=for-the-badge&logo=flutter&logoColor=white" alt="Flutter" />
  <img src="https://img.shields.io/badge/Dart-3.13+-0175C2?style=for-the-badge&logo=dart&logoColor=white" alt="Dart" />
  <img src="https://img.shields.io/badge/Platform-Android%20%7C%20iOS%20%7C%20Web-4E73DF?style=for-the-badge" alt="Platform" />
  <img src="https://img.shields.io/badge/Tests-12%2F12%20Passed-28A745?style=for-the-badge&logo=githubactions&logoColor=white" alt="Tests" />
  <img src="https://img.shields.io/badge/Design-Tiranga%20System-FF9933?style=for-the-badge" alt="Design" />
</p>

---

## 📑 Table of Contents
- [About Sahaayak](#-about-sahaayak)
- [Why Sahaayak? (The Problem & Solution)](#-why-sahaayak-the-problem--solution)
- [Core Differentiators](#-core-differentiators)
  - [1. FairMatch AI Matching Engine](#1-fairmatch-ai-matching-engine)
  - [2. Transparent 5-Way Split & Welfare Wallet](#2-transparent-5-way-split--welfare-wallet)
  - [3. Cooperative Trust & 4-Stage Verification](#3-cooperative-trust--4-stage-verification)
  - [4. AI Demand Forecasting & Allocation Nudges](#4-ai-demand-forecasting--allocation-nudges)
- [Four Integrated Roles](#-four-integrated-roles)
- [Technology Stack](#-technology-stack)
- [Project Architecture](#-project-architecture)
- [Getting Started & Installation](#-getting-started--installation)
- [Test Credentials & Demo Accounts](#-test-credentials--demo-accounts)
- [Automated Tests](#-automated-tests)
- [Regulatory & Ethical Compliance](#-regulatory--ethical-compliance)
- [Hackathon & Team Details](#-hackathon--team-details)

---

## 💡 About Sahaayak

Private gig economy platforms extract **20% to 30% commissions**, offer opaque black-box dispatching, and leave informal gig workers with zero institutional ownership, job security, or health benefits.

Meanwhile, India has thousands of registered **Labour Cooperative Societies** and **Federations** with certified, skilled tradespeople (electricians, plumbers, carpenters, technicians, cleaners), but they lack modern digital routing, mobile booking, and real-time governance tools.

**Sahaayak (सहायक)** bridges this gap. It is an open, institutional digital operating system owned by the cooperative ecosystem, ensuring:
- **78% direct take-home pay** to workers.
- **Fair workload allocation** preventing algorithmic starvation.
- **Built-in social safety net** (group micro-insurance & welfare funds per job).
- **100% democratic transparency** for primary societies and state federations.

---

## 🌟 Core Differentiators

### 1. FairMatch AI Matching Engine
Unlike profit-maximizing platforms that overload a top 5% star-tier while starving new or average workers, Sahaayak features a **two-stage explainable matching pipeline**:
- **Stage A (Hard Filters):** Skill compatibility, cooperative certification, active availability, and geo-proximity.
- **Stage B (Multi-Factor Scoring):** 
  $$\text{Score} = w_s \cdot \text{Skill} + w_d \cdot \text{Distance} + w_a \cdot \text{Availability} + w_c \cdot \text{Cert} + w_q \cdot \text{Rating} + w_f \cdot \text{Fairness}$$
- **Explainable Radar Chart:** Customers can tap *"Why this worker?"* to view an interactive radar chart breaking down exactly why the worker was recommended.

### 2. Transparent 5-Way Split & Welfare Wallet
Every completed job automatically divides the service fee transparently:
- 👷 **Worker:** **78%** (Direct instant payout)
- 🏢 **Primary Society:** **12%** (Local cooperative operations & support)
- 🛡️ **Worker Welfare Fund:** **5%** (Credited straight into the worker's Welfare Wallet for healthcare & tool subsidies)
- 🏥 **Group Insurance:** **3%** (Active ₹5,00,000 partner micro-insurance cover)
- 🏛️ **Federation Reserve:** **2%** (Inter-society emergency pool & apprentice training)

### 3. Cooperative Trust & 4-Stage Verification
- Strict cooperative pipeline: `Unverified` ➔ `Submitted` ➔ `Under Review` ➔ `Cooperative Verified`.
- In-person and physical document verification by primary cooperative society administrators.
- **Zero Aadhaar Number Retention:** Full DPDP Act compliance with strict data export and privacy preservation.

### 4. AI Demand Forecasting & Allocation Nudges
- 7-day rolling seasonal-naive moving-average projections per society × service category × locality.
- Automated workforce allocation nudges sent to cooperative administrators to proactively prevent service shortages.

---

## 👥 Four Integrated Roles

| Role | Target User | Key Capabilities |
|---|---|---|
| **Citizen / Customer** | Household / Business clients | Smart booking, AI category classification, transparent pricing, FairMatch radar chart, UPI checkout, digital GST cooperative invoice |
| **Cooperative Worker** | Electricians, Plumbers, Trades | Job dispatch with countdown, turn-by-turn map navigation, live earnings breakdown, Welfare Wallet balance & insurance claims |
| **Society Admin** | Primary Cooperative Societies | Worker onboarding & verification queue, active duty roster, society revenue analytics, local demand alerts |
| **Federation Admin** | District / State Federations | Cross-society governance, Gini workload fairness index, live FairMatch slider weights tuning & real-time booking simulation |

---

## 🛠️ Technology Stack

| Layer | Technology |
|---|---|
| **Framework** | **Flutter 3.47+** (Dart 3.13+, Sound Null-Safety) |
| **State Management** | **Flutter Riverpod** (Declarative, testable, reactive state) |
| **Routing** | **GoRouter** (Declarative routing with role-based route guards) |
| **Backend & Auth** | **Firebase** (Auth with phone/Google, Cloud Firestore with offline cache, Storage) |
| **Geospatial & Maps** | **flutter_map** + **latlong2** (OpenStreetMap) & **geolocator** |
| **Charts & Analytics** | **fl_chart** (Interactive radar charts, 5-way split donut pie charts, demand curves) |
| **Invoice & PDF** | **pdf** + **printing** (Official GST cooperative digital invoice generation) |
| **Speech & Voice** | **speech_to_text** (Voice query input) & **flutter_tts** (Voice read-aloud) |
| **Localization** | Multi-lingual ARB: **English**, **Hindi (हिन्दी)**, and **Marathi (मराठी)** |

---

## 📁 Project Architecture

```
lib/
├── core/
│   ├── models/           # Data models: User, WorkerProfile, Booking, Config
│   ├── router/           # GoRouter configuration & role-based route guards
│   ├── services/         # FairMatchService, EarningsSplitService, ForecastingService
│   ├── theme/            # Tiranga Design System (Saffron, Navy, Green, Surface)
│   └── widgets/          # TricolourRibbon, ChakraWatermark, Error & Offline banners
├── features/
│   ├── auth/             # Login, OTP, Role Selection, Worker 7-Step Registration Wizard
│   ├── customer/         # Booking Flow, FairMatch Funnel, Tracking, Payment & Invoice
│   ├── worker/           # Worker Dashboard, Active Job, Welfare Wallet & Claims
│   ├── society_admin/    # Society Dashboard, Worker Registry & Verification Pipeline
│   ├── federation_admin/ # Federation Dashboard, Gini Index, Live Weight Sliders & Simulator
│   └── shared/           # AI Voice Assistant, Settings, Theme, DPDP Privacy Tools
└── l10n/                 # Localization ARB files (en, hi, mr)
```

---

## 🚀 Getting Started & Installation

### Prerequisites
- **Flutter SDK:** 3.47.5 or higher (`flutter doctor`)
- **Dart SDK:** 3.13.4 or higher
- **Android Studio / VS Code** with Flutter & Dart plugins
- **Android Device or Emulator** (API 26+) or Chrome/Desktop

### Quick Start
```bash
# 1. Clone the repository
git clone https://github.com/YOUR_USERNAME/sahaayak.git
cd sahaayak

# 2. Install dependencies
flutter pub get

# 3. Verify code health
flutter analyze

# 4. Run tests
flutter test

# 5. Launch the app
flutter run
```

### Build Release APK
```bash
flutter build apk --release
# Generated APK: build/app/outputs/flutter-apk/app-release.apk
```

---

## 🔑 Test Credentials & Demo Accounts

The app includes built-in test accounts that bypass SMS gateways with OTP: **`123456`**. You can also tap the **quick one-tap demo role buttons** on the Login screen:

| Role | Demo User | Test Phone | OTP | Scenario / Society |
|---|---|---|---|---|
| **Citizen** | Rohan Deshmukh | `+91 90000 00001` | `123456` | Household client in Kothrud, Pune |
| **Worker** | Rajesh Kumar | `+91 90000 00002` | `123456` | Master Electrician (Verified, 8 yrs exp) |
| **Society Admin** | Suresh Patil | `+91 90000 00003` | `123456` | Kothrud Shramik Sahakari Sanstha |
| **Federation Admin** | Dr. Anand Joshi | `+91 90000 00004` | `123456` | Maharashtra State Labour Federation |
| **Worker (Trainee)** | Sunita More | `+91 90000 00005` | `123456` | Domestic Specialist (Verification in progress) |

---

## 🧪 Automated Tests

The repository maintains an automated test suite verifying core business logic:
- `test/unit/fairmatch_test.dart` — Validates Stage A filters, Stage B radar scores, and Haversine geo-distance.
- `test/unit/earnings_split_test.dart` — Tests 5-way split arithmetic and ledger balancing.
- `test/unit/forecasting_test.dart` — Tests 7-day seasonal-naive demand projections.
- `test/unit/demo_path_integration_test.dart` — End-to-end execution of the primary demo pathway.
- `test/widget_test.dart` — App startup, branding elements, and navigation tests.

Run tests anytime with:
```bash
flutter test
```

---

## ⚖️ Regulatory & Ethical Compliance
1. **Zero Government Pretense:** Sahaayak is an independent digital cooperative operating platform and makes no unauthorized claims of UIDAI or central government endorsement.
2. **DPDP Compliance:** No 12-digit Aadhaar numbers are ever collected or stored. Worker identity verification is strictly performed via in-person cooperative society document review.
3. **Transparent Auditing:** Every rupee from the customer fee is accounted for in a cryptographically trackable 5-way digital invoice.

---

## 🏆 Hackathon & Credits
- **Initiative:** Smart India Hackathon (SIH)
- **Problem Statement ID:** SIH26089 — Digital Platform for Labour Cooperatives
- **Theme:** Cooperative Economy, Gig Worker Welfare, Explainable AI
