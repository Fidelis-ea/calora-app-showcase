# calora-app-showcase

# 🏃 Calora (Mobile Health & Nutrition App)

> **Note:** This repository is a portfolio showcase only. The complete source code is kept private to protect academic integrity and intellectual property related to the Final Project (Tugas Akhir). If you are a recruiter or hiring manager interested in the implementation details, feel free to contact me.

## 📱 About Calora

**Calora** adalah aplikasi mobile untuk membantu pengguna mengelola pola hidup sehat melalui pemantauan kalori, nutrisi, aktivitas fisik, dan perkembangan kesehatan.

Aplikasi ini dikembangkan sebagai proyek Tugas Akhir dengan fokus pada pengalaman pengguna (User Experience), kemudahan pencatatan aktivitas kesehatan, serta pemanfaatan teknologi AI untuk membantu analisis makanan dan konsultasi kesehatan.

---

## 📥 Try The App

Anda dapat mencoba aplikasi melalui:

- 📱 **Android APK:** [Download APK](https://github.com/Fidelis-ea/calora-app-showcase/releases/tag/v1.0.0)

---

## ✨ Key Features

Calora memiliki beberapa fitur utama:

- 🔐 **Authentication**
  - Registrasi dan login pengguna.
  - Pengelolaan profil kesehatan pengguna.

- 🍱 **Food Tracking**
  - Pencatatan makanan harian.
  - Perhitungan informasi kalori dan nutrisi.
  - Riwayat konsumsi makanan.

- 📸 **AI Food Scan**
  - Membantu mengenali makanan menggunakan teknologi AI.
  - Memberikan informasi estimasi nutrisi dari makanan.

- 🏃 **Activity Tracker**
  - Mencatat aktivitas olahraga.
  - Memantau perkembangan aktivitas pengguna.

- 📊 **Nutrition Dashboard**
  - Menampilkan ringkasan konsumsi kalori.
  - Melihat perkembangan pola makan.

- 🤖 **AI Health Assistant**
  - Chatbot AI untuk membantu menjawab pertanyaan seputar nutrisi dan gaya hidup sehat.

- 📷 **Progress Photo**
  - Menyimpan dokumentasi perkembangan fisik pengguna.

---

## 📸 Screenshots

<img width="720" height="1429" alt="login" src="https://github.com/user-attachments/assets/f08529e3-4f98-4bfd-9117-99fda9cc0de2" />
<img width="576" height="1154" alt="dashboard" src="https://github.com/user-attachments/assets/1bbf0e5a-c2a3-455e-92fd-a8f72021c78f" />
<img width="720" height="1434" alt="scan makanan" src="https://github.com/user-attachments/assets/98e656ba-5ff3-4c22-a4e0-9c2d16d9a4f4" />
<img width="576" height="1161" alt="progres photo" src="https://github.com/user-attachments/assets/1898fd78-2d5e-4246-b812-7b8722e619ae" />
<img width="576" height="1155" alt="profile" src="https://github.com/user-attachments/assets/0db2140b-6202-4076-9143-e604022a7974" />
<img width="576" height="1154" alt="chatbot" src="https://github.com/user-attachments/assets/f760df1b-54de-4f6c-a509-1253552b720a" />

<img width="720" height="1448" alt="kategori" src="https://github.com/user-attachments/assets/72041fcb-2a0e-4036-82f5-a6529faa9796" />




---

# 🛠️ Tech Stack

## Mobile Development

- Flutter
- Dart
- Material Design 3

## Backend & Database

- Firebase Authentication
- Cloud Firestore

## AI Integration

- Gemini AI API

## Design

- Figma
- Neubrutalism UI Design

---

# 🏗️ Application Architecture

Calora menggunakan pendekatan modular dengan pemisahan antara:

- UI Layer
- Business Logic
- Data Management

Struktur utama aplikasi:
lib/

├── screens/
│ ├── home/
│ ├── login/
│ ├── scan/
│ └── profile/

├── models/

├── services/

├── widgets/

└── utils/


---

# 🧠 Challenges & Learnings

Selama pengembangan Calora, beberapa tantangan yang berhasil diselesaikan:

### 1. Integrasi AI Food Scan

Menghubungkan aplikasi Flutter dengan AI API untuk membantu mengenali makanan dan menghasilkan informasi nutrisi.

### 2. Pengelolaan Data Kesehatan Pengguna

Membuat struktur database yang mampu menyimpan data pengguna seperti:

- Riwayat makanan.
- Aktivitas olahraga.
- Progress pengguna.
- Riwayat scan makanan.

### 3. Pengembangan UI Mobile

Menerapkan desain UI yang konsisten agar pengguna mudah melakukan pencatatan aktivitas kesehatan.

---

# 💻 Code Quality Example

Source code utama tidak tersedia pada repository ini. Berikut contoh sederhana gaya penulisan kode yang digunakan dalam pengembangan Calora.

```dart
class FoodModel {
  final String name;
  final int calories;
  final double protein;
  final double carbs;
  final double fat;

  FoodModel({
    required this.name,
    required this.calories,
    required this.protein,
    required this.carbs,
    required this.fat,
  });

  factory FoodModel.fromJson(Map<String, dynamic> json) {
    return FoodModel(
      name: json['name'] ?? '',
      calories: json['calories'] ?? 0,
      protein: (json['protein'] ?? 0).toDouble(),
      carbs: (json['carbs'] ?? 0).toDouble(),
      fat: (json['fat'] ?? 0).toDouble(),
    );
  }
}
