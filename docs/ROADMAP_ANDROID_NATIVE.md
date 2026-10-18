# Roadmap Belajar Android Native

> Jalur belajar untuk developer yang sudah mengenal JavaScript, TypeScript, dan Node.js, dengan target membuat aplikasi Android native menggunakan Kotlin dan Jetpack Compose.

## Target akhir

Mampu membangun aplikasi Android, menggunakan API dan database, melakukan debugging di perangkat Android fisik, serta menghasilkan APK debug dan release.

- **Bahasa:** Kotlin
- **IDE:** Android Studio
- **UI:** Jetpack Compose + Material 3
- **Build:** Gradle + Android SDK
- **Estimasi:** 6–8 minggu, 1–2 jam per hari

## 1. Persiapan tools

1. **Android Studio** — editor, UI tools, debugger, dan build APK. [Download](https://developer.android.com/studio)
2. **Kotlin** — bahasa pemrograman utama. [Kotlin Tour](https://kotlinlang.org/docs/kotlin-tour-welcome.html)
3. **Android SDK + ADB** — build aplikasi, instal APK, sambungkan perangkat, dan baca log. [ADB docs](https://developer.android.com/tools/adb)
4. **Git** — version control. [Download](https://git-scm.com/downloads)

Android Studio biasanya menyediakan JDK yang diperlukan Gradle. Untuk pengujian di HP, aktifkan Developer options dan USB debugging, sambungkan dengan USB, lalu izinkan debugging.

## 2. Roadmap mingguan

### Minggu 1 — Kotlin untuk developer TypeScript

Pelajari:
- `val`, `var`, tipe data, kondisi, perulangan, dan fungsi.
- `class`, `data class`, interface, dan extension functions.
- Null safety: `String?`, `?.`, `?:`, dan `!!`.
- Collections, lambda, generics, dan exception handling.
- Dasar coroutine dan fungsi `suspend`.

**Proyek latihan:** kalkulator sederhana berbasis console.

**Catatan:** pahami perbedaan nullability Kotlin dengan TypeScript; jangan hanya menghafalkan sintaks.

### Minggu 2 — UI dengan Jetpack Compose

Pelajari:
- `@Composable`, `Text`, `Button`, dan `Image`.
- Layout `Column`, `Row`, `Box`, dan `Modifier`.
- Material 3, warna, typography, dan tema gelap.
- Input teks, form, validasi, dan aksi tombol.
- State menggunakan `remember` dan `mutableStateOf`.

**Proyek latihan:** aplikasi profil dengan tema dark, tombol interaktif, dan form sederhana.

### Minggu 3 — Navigasi dan struktur aplikasi

Pelajari:
- Navigasi antarlayar dan pengiriman data.
- `ViewModel` dan `StateFlow`.
- UI state: loading, success, dan error.
- Lifecycle dasar dan pemisahan UI dari business logic.

**Proyek latihan:** aplikasi catatan dengan layar daftar, detail, dan tambah catatan.

**Catatan:** pisahkan file UI, model, dan ViewModel; hindari menaruh semua kode dalam satu `MainActivity.kt`.

### Minggu 4 — Penyimpanan data

Pelajari:
- DataStore untuk preferensi sederhana.
- Room untuk database lokal berbasis SQLite.
- CRUD: Create, Read, Update, Delete.
- Repository pattern dan pemisahan data layer.

**Proyek latihan:** to-do list yang datanya tetap tersimpan setelah aplikasi ditutup dan dibuka kembali.

### Minggu 5 — API dan networking

Pelajari:
- HTTP, REST API, dan JSON.
- Retrofit untuk request ke server.
- Coroutines untuk operasi asynchronous.
- Parsing respons, error handling, dan timeout.
- Permission internet dan pemuatan gambar.

**Proyek latihan:** katalog yang mengambil data dari API dan menampilkan daftar serta detail item.

### Minggu 6 — Fitur perangkat dan debugging

Pelajari:
- Runtime permissions.
- Memilih file atau gambar dari perangkat.
- Notifikasi dasar.
- Logcat dan debugger.
- Testing fungsi, ViewModel, dan UI.
- Git untuk version control.

**Proyek latihan:** aplikasi catatan yang memungkinkan pengguna memilih gambar dari HP.

### Minggu 7–8 — Proyek final dan distribusi APK

Gabungkan materi sebelumnya:
- UI konsisten dan navigasi.
- Database lokal atau integrasi API.
- Loading, empty state, dan error handling.
- Pengujian di HP fisik.
- App icon, nama aplikasi, dan versioning.
- Build APK debug dan release.

**Proyek final:** aplikasi katalog, task manager, atau client API dengan desain sendiri.

## 3. Referensi resmi

- [Android Basics with Compose](https://developer.android.com/courses/android-basics-compose/course) — kursus dari dasar Kotlin hingga aplikasi Android.
- [Kotlin Tour](https://kotlinlang.org/docs/kotlin-tour-welcome.html) — sintaks Kotlin.
- [Jetpack Compose](https://developer.android.com/develop/ui/compose) — dokumentasi UI, state, layout, dan komponen.
- [Codelab aplikasi Android pertama](https://developer.android.com/codelabs/basic-android-kotlin-compose-first-app) — panduan praktik.
- [Android Debug Bridge (ADB)](https://developer.android.com/tools/adb) — komunikasi PC dengan perangkat Android.

## 4. Praktik pertama

1. Buka Android Studio lalu pilih **New Project → Empty Activity**.
2. Pilih Kotlin dan konfigurasi Compose dari template.
3. Beri nama proyek, misalnya `NativeStarter`.
4. Tunggu Gradle selesai sinkronisasi.
5. Sambungkan HP dengan USB debugging atau jalankan emulator.
6. Tekan **Run ▶** untuk menginstal dan menjalankan aplikasi.

## 5. Build APK

### APK debug

1. Buka menu **Build** di Android Studio.
2. Pilih opsi **Build APK(s)** yang tersedia.
3. Tunggu build selesai, lalu buka lokasi file dari notifikasi Android Studio.

Lokasi umum:

```text
app/build/outputs/apk/debug/app-debug.apk
```

### APK release

Gunakan **Generate Signed App Bundle or APK**, lalu pilih APK jika ingin membagikan file instalasi langsung. Simpan signing key dengan aman dan jangan masukkan password atau keystore pribadi ke repository publik.

Jika ingin menerbitkan aplikasi di Google Play, pelajari Android App Bundle (AAB), signing, dan persyaratan publikasi terbaru.

## 6. Checklist kompetensi

- [ ] **Kotlin:** membuat fungsi, class, data class, dan menangani null safety.
- [ ] **Compose UI:** membuat form, tombol, daftar, dan tema aplikasi.
- [ ] **Arsitektur:** memisahkan UI, ViewModel, dan repository.
- [ ] **Database:** data tetap tersimpan setelah aplikasi ditutup.
- [ ] **API:** menampilkan data server dan menangani error.
- [ ] **Testing:** membaca Logcat dan memperbaiki crash.
- [ ] **APK:** build, menginstal, dan menguji APK di HP.

## Prinsip belajar

Jangan mempelajari seluruh Android API sekaligus. Mulai dari Kotlin dasar, buat satu UI sederhana, lalu tambahkan satu kemampuan pada satu waktu. Pengalaman TypeScript membantu pada fungsi, objek, asynchronous programming, dan API; fokuskan waktu pada konsep baru Android.
