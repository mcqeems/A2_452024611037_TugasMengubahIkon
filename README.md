# Aplikasi Affirmations

Solusi kode untuk pelatihan Android Basics with Compose: aplikasi Affirmations.
Proyek ini juga digunakan sebagai bahan pembelajaran untuk mengubah ikon
aplikasi adaptif (Adaptive Icon) pada aplikasi Android.


## Deskripsi

Aplikasi Affirmations adalah aplikasi Android sederhana yang menampilkan daftar
kartu berisi kalimat-kalimat afirmasi positif yang dapat di-scroll. Aplikasi ini
terdiri dari 10 kartu, di mana setiap kartu menampilkan sebuah gambar beserta
teks afirmasi yang menyertainya. Selain itu, proyek ini menjadi sarana latihan
untuk memahami cara mengganti dan mengonfigurasi Adaptive Icon aplikasi
Android agar tampilannya dapat menyesuaikan bentuk bulat, kotak membulat,
ataupun bentuk lainnya sesuai dengan launcher perangkat.


## Fitur

- Menampilkan daftar 10 kartu afirmasi dalam bentuk daftar yang dapat di-scroll.
- Setiap kartu berisi gambar dan teks afirmasi.
- Mendukung tema terang dan tema gelap.
- Dibangun sepenuhnya menggunakan Jetpack Compose dan Material 3.
- Mendukung Adaptive Icon yang tampil secara adaptif pada berbagai launcher
  Android, dengan kombinasi antara `ic_launcher_foreground.xml` sebagai
  lapisan depan dan `ic_launcher_background.xml` sebagai lapisan belakang.


## Teknologi yang Digunakan

- Bahasa pemrograman Kotlin
- Jetpack Compose
- Material Design 3
- LazyColumn untuk daftar yang dapat di-scroll
- Android Studio (IDE)
- Gradle dengan Kotlin DSL


## Struktur Proyek

```
app/src/main/java/com/example/affirmations/
├── MainActivity.kt        // Activity utama dan composable utama aplikasi
├── data/
│   └── Datasource.kt      // Sumber data daftar afirmasi
├── model/
│   └── Affirmation.kt     // Data class untuk merepresentasikan satu afirmasi
└── ui/
    └── theme/
        ├── Color.kt       // Definisi warna untuk tema
        └── Theme.kt       // Konfigurasi tema terang dan gelap
```


## Prasyarat

Sebelum menjalankan proyek ini, pastikan Anda telah memiliki:

- Pemahaman dasar tentang Kotlin
- Pemahaman tentang List di Kotlin
- Pengalaman membangun tampilan dengan Jetpack Compose
- Pemahaman dasar tentang resource Android, khususnya struktur ikon aplikasi
- Android Studio versi terbaru
- Perangkat atau emulator Android (minSdk 24)


## Pembelajaran: Mengubah Adaptive Icon

Bagian ini menjelaskan langkah-langkah untuk mengubah ikon aplikasi adaptif
pada proyek ini. Adaptive Icon adalah ikon yang secara otomatis menyesuaikan
bentuknya (bulat, squircle, dan lain-lain) mengikuti tema launcher perangkat.

1. Siapkan dua aset gambar, yaitu:
   - `ic_launcher_foreground.xml` yang berada di
     `app/src/main/res/drawable/` sebagai lapisan depan (foreground).
   - `ic_launcher_background.xml` yang berada di
     `app/src/main/res/drawable/` sebagai lapisan belakang (background).
2. Perbarui file `app/src/main/res/mipmap-anydpi-v26/ic_launcher.xml` dan
   `ic_launcher_round.xml` untuk menentukan lapisan foreground dan background
   yang digunakan.
3. Pastikan pada `AndroidManifest.xml`, atribut `android:icon` dan
   `android:roundIcon` tetap mengarah ke `@mipmap/ic_launcher` dan
   `@mipmap/ic_launcher_round`.
4. Bangun ulang proyek dan lihat perubahan ikon pada launcher perangkat atau
   emulator.

Dengan memahami alur di atas, Anda dapat dengan mudah mengganti ikon
aplikasi pada proyek Android apa pun yang sudah menggunakan Adaptive Icon.


## Cara Menjalankan

1. Pastikan Android Studio sudah terpasang di komputer Anda.
2. Clone atau unduh repositori ini.
3. Buka proyek melalui Android Studio.
4. Tunggu hingga proses sinkronisasi Gradle selesai.
5. Hubungkan perangkat Android atau jalankan emulator.
6. Klik tombol Run untuk membangun dan menjalankan aplikasi.
