# 🐄 DesiMoo: Innovating India’s Dairy through Intelligence

![Flutter](https://img.shields.io/badge/Frontend-Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Language-Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)
![TensorFlow Lite](https://img.shields.io/badge/Edge_AI-TFLite-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![MongoDB](https://img.shields.io/badge/Database-MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![Status](https://img.shields.io/badge/Status-Hackathon_Ready-success?style=for-the-badge)

**DesiMoo** is a comprehensive, AI-driven mobile application designed to empower rural Indian farmers. By bridging the digital divide with offline AI and inclusive voice technology, DesiMoo transforms how livestock is identified, managed, and traded.

## ✨ Why DesiMoo?
In rural India, internet connectivity is often unreliable, and technological literacy can be a barrier. DesiMoo solves this by leveraging **On-Device Edge AI**, meaning its core cattle-scanning features work with **zero latency and zero internet dependency**. Combined with a multilingual Text-to-Speech (TTS) assistant, the app actually *speaks* to the farmers in their native tongue, guiding them every step of the way.

---

## 🚀 Key Features

* 🧠 **Offline Edge AI Scanner:** Powered by a custom **YOLOv8** model exported to `float16` TFLite. It instantly identifies indigenous cow and buffalo breeds directly on the device.
* 🗣️ **Multilingual Voice Assistant:** Built-in Flutter TTS engine that reads out app navigation, breed details, and health warnings dynamically in **English, Hindi, and Marathi**.
* 🩺 **Smart Cattle Care:** Instantly generates tailored diet recommendations and alerts farmers about breed-specific disease vulnerabilities (e.g., Mastitis, FMD) upon scanning.
* 🏷️ **Pashu Aadhaar Registry:** A robust admin portal connected to **MongoDB Cloud**, allowing seamless linking of cattle to a farmer's National ID for official record-keeping.
* 🛒 **Pashu Mandi (Marketplace):** A peer-to-peer decentralized trading platform where farmers can seamlessly buy and sell cattle with integrated direct-contact features.
* 📚 **Interactive Breed Library:** A rich, filterable catalog of top indigenous Indian cattle and buffalo breeds (with Camel support coming soon!).

---

## 🛠️ Tech Stack & Architecture

### **Frontend**
* **Framework:** Flutter & Dart (Cross-platform UI)
* **State Management:** ValueNotifier (Lightweight, reactive state)
* **Accessibility:** `flutter_tts` (Dynamic Text-to-Speech)

### **Edge AI & Computer Vision**
* **Model:** YOLOv8 (`best_float16.tflite`)
* **Engine:** `tflite_flutter`
* **Pipeline:** Custom tensor preprocessing using `image_cropper` and `image` packages to decode, resize (640x640), and normalize RGB matrices for neural network input.

### **Backend & Cloud**
* **Database:** MongoDB Atlas (NoSQL)
* **Driver:** `mongo_dart`

---

## 🎯 How It Works
1. **Scan:** The farmer snaps a photo of their cattle.
2. **Process:** The local TFLite model processes the tensor array and identifies the breed.
3. **Assist:** The app displays the breed's origin, lifespan, and milk capacity, while the **Voice Assistant** reads out the recommended diet and potential diseases in the farmer's local language.
4. **Manage:** The cattle is saved to the local dashboard, registered to Pashu Aadhaar, or listed on the Pashu Mandi for sale!

---
> *Built with ❤️ for India's unsung heroes—our farmers.*
