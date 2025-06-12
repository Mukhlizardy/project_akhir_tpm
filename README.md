# Travel Assistant App

Aplikasi mobile Travel Assistant yang dikembangkan dengan Flutter untuk memenuhi tugas mata kuliah Teknologi dan Pemrograman Mobile.

## Fitur Utama

### ✅ Persyaratan yang Terpenuhi:

1. **Login dengan Enkripsi & Session**

   - Autentikasi menggunakan enkripsi SHA-256
   - Session management dengan SharedPreferences
   - Tidak menggunakan Firebase

2. **Local Storage**

   - Menyimpan data user dan preferensi
   - Riwayat feedback dan saran
   - Data offline tetap tersedia

3. **Web Service/API**

   - Simulasi API untuk pencarian destinasi
   - HTTP requests untuk data mata uang
   - Real-time data processing

4. **Bottom Navigation**

   - **Home**: Pencarian destinasi dengan sensor accelerometer
   - **Currency**: Konversi mata uang (USD, IDR, EUR, GBP, JPY)
   - **Time Zone**: Konversi waktu (WIB, WITA, WIT, London, New York)
   - **Profile**: Profil user dengan foto, feedback, dan logout

5. **Konversi Mata Uang**

   - Minimal 5 mata uang: USD, IDR, EUR, GBP, JPY
   - Real-time conversion dengan exchange rates
   - Swap currencies dengan mudah

6. **Konversi Waktu**

   - WIB, WITA, WIT, London, New York
   - Real-time clock untuk semua zona waktu
   - Format waktu dan tanggal yang user-friendly

7. **Pencarian & Notifikasi**

   - Pencarian destinasi travel
   - Notifikasi saat memilih destinasi
   - Notifikasi saat device di-shake

8. **Sensor Accelerometer**
   - Mendeteksi gerakan shake
   - Menampilkan data sensor real-time
   - Trigger notifikasi berdasarkan gerakan

## Instalasi

### Prasyarat

- Flutter SDK >= 3.10.0
- Dart SDK >= 3.0.0
- Android Studio atau VS Code
- Android device/emulator

### Langkah Instalasi

1. **Clone atau buat project baru**

   ```bash
   flutter create travel_assistant_app
   cd travel_assistant_app
   ```

2. **Ganti file `pubspec.yaml`** dengan konfigurasi dependencies yang disediakan

3. **Ganti file `lib/main.dart`** dengan kode aplikasi yang disediakan

4. **Update `android/app/src/main/AndroidManifest.xml`** dengan konfigurasi permissions

5. **Install dependencies**

   ```bash
   flutter pub get
   ```

6. **Jalankan aplikasi**
   ```bash
   flutter run
   ```

## Cara Penggunaan

### 1. Login/Register

- Masukkan username dan password
- Untuk user baru, akan otomatis register
- Password dienkripsi dengan SHA-256

### 2. Home Screen

- Gunakan search bar untuk mencari destinasi
- Lihat data accelerometer real-time
- Shake device untuk mendapat notifikasi

### 3. Currency Converter

- Pilih mata uang asal dan tujuan
- Masukkan jumlah untuk konversi
- Gunakan tombol swap untuk menukar mata uang

### 4. Time Zone Converter

- Pilih zona waktu dari dropdown
- Lihat waktu real-time semua zona waktu
- Tap zona waktu untuk set sebagai fokus

### 5. Profile

- Lihat informasi profil
- Berikan feedback untuk mata kuliah
- Lihat riwayat feedback
- Logout dari aplikasi

## Teknologi yang Digunakan

- **Flutter**: Framework UI cross-platform
- **Dart**: Bahasa pemrograman
- **SharedPreferences**: Local storage
- **Crypto**: Enkripsi password
- **HTTP**: Web service communication
- **Flutter Local Notifications**: Push notifications
- **Sensors Plus**: Accelerometer sensor
- **Permission Handler**: Runtime permissions

## Struktur Aplikasi

```
lib/
├── main.dart                 # Entry point aplikasi
├── screens/
│   ├── splash_screen.dart    # Splash screen
│   ├── login_screen.dart     # Login/Register
│   ├── main_screen.dart      # Bottom navigation
│   ├── home_screen.dart      # Search & sensor
│   ├── currency_screen.dart  # Currency converter
│   ├── time_screen.dart      # Time zone converter
│   └── profile_screen.dart   # Profile & feedback
├── services/
│   ├── auth_service.dart     # Authentication
│   ├── storage_service.dart  # Local storage
│   └── api_service.dart      # Web services
└── models/
    ├── user_model.dart       # User data model
    └── destination_model.dart # Destination model
```

## Fitur Keamanan

- Password encryption dengan SHA-256
- Session management yang aman
- Input validation
- Error handling yang robust

## Testing

Untuk menjalankan tests:

```bash
flutter test
```

## Build APK

Untuk membuat APK:

```bash
flutter build apk --release
```

## Catatan Penting

1. **Permissions**: Pastikan aplikasi memiliki permission untuk internet dan notifikasi
2. **Sensor**: Accelerometer hanya berfungsi pada device fisik, tidak pada emulator
3. **Notifikasi**: Pastikan notifikasi diizinkan di pengaturan device
4. **Internet**: Diperlukan untuk simulasi API calls

## Troubleshooting

### Masalah Umum:

1. **Sensor tidak berfungsi**

   - Pastikan menggunakan device fisik
   - Check permission di pengaturan

2. **Notifikasi tidak muncul**

   - Enable notifikasi di pengaturan device
   - Check permission aplikasi

3. **Build error**
   - Jalankan `flutter clean` dan `flutter pub get`
   - Update Flutter ke versi terbaru

## Kontribusi

Aplikasi ini dibuat untuk tujuan pembelajaran mata kuliah Teknologi dan Pemrograman Mobile.

## Lisensi

MIT License - Silakan gunakan untuk tujuan pembelajaran.

---

**Catatan**: Aplikasi ini dibuat sebagai contoh implementasi berbagai teknologi mobile programming dan memenuhi semua persyaratan yang diminta dalam tugas mata kuliah.
