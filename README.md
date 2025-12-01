# 🏀 AR Basketball Visualization (Project UAS)

> **Aplikasi Augmented Reality berbasis Android untuk memvisualisasikan produk bola basket 3D secara real-time menggunakan metode Marker-based Tracking.**

![Unity](https://img.shields.io/badge/Unity-2022.3%20LTS-black?style=flat&logo=unity)
![Platform](https://img.shields.io/badge/Platform-Android-green?style=flat&logo=android)
![AR](https://img.shields.io/badge/SDK-AR%20Foundation-blue)

## 📖 Deskripsi Proyek
Proyek ini dikembangkan untuk memenuhi tugas akhir mata kuliah **Desain AR/VR**. Aplikasi ini bertujuan untuk mendemonstrasikan bagaimana teknologi AR dapat digunakan dalam pemasaran produk olahraga. 

Pengguna dapat memindai bola basket fisik (khususnya merek Spalding) menggunakan kamera *smartphone*, dan aplikasi akan memunculkan model 3D digital yang presisi dan bertekstur tinggi tepat di atas bola nyata tersebut (*Image Tracking*).

## ✨ Fitur Utama
* **Marker-based Tracking:** Mendeteksi logo spesifik "SPALDING NBA" pada permukaan bola yang melengkung.
* **Real-time Rendering:** Menampilkan objek 3D bola basket dengan tekstur realistis secara instan saat marker terdeteksi.
* **Automatic Scaling:** Objek 3D disesuaikan ukurannya (0.24m) agar pas dengan ukuran bola asli.
* **Stabilisasi:** Menggunakan ARCore untuk menjaga posisi objek tetap menempel pada marker meski kamera bergerak.

## 🛠️ Teknologi yang Digunakan
* **Game Engine:** Unity 2022.3 LTS
* **AR Framework:** AR Foundation 5.x
* **Plugin:** Google ARCore XR Plugin
* **Bahasa Pemrograman:** C#
* **Desain 3D:** Blender / Polycam (untuk aset model)
* **Version Control:** Git & GitHub

## 📂 Struktur Repository
Sesuai standar pengumpulan tugas, struktur folder proyek ini disusun sebagai berikut:

| Folder | Deskripsi |
| :--- | :--- |
| 📁 **`src`** | Berisi *Source Code* lengkap project Unity (`Assets`, `Packages`, `ProjectSettings`). Folder ini bersih dari file sampah (*Library/Temp*). |
| 📁 **`build`** | Berisi file aplikasi mentah (`.apk`) yang siap diinstal di HP Android. |
| 📁 **`docs`** | Berisi dokumen pendukung seperti Laporan Akhir (PDF) dan Slide Presentasi (PPT). |
| 📁 **`assets`** | Berisi aset mentah seperti foto marker asli (`.jpg`) dan model 3D (`.fbx`) sebelum diimpor ke Unity. |
| 📁 **`demo`** | (Opsional) Video demonstrasi penggunaan aplikasi. |

## 🚀 Cara Instalasi & Menjalankan Aplikasi

### Persiapan Perangkat
* Smartphone Android (Minimal Android 7.0 "Nougat").
* Mendukung Google Play Services for AR (ARCore).

### Langkah Instalasi
1.  Buka folder [`/build`](./build) di repository ini.
2.  Download file bernama **`FinalAR_Basket.apk`** (atau nama file APK kamu).
3.  Kirim file tersebut ke HP Android kamu.
4.  Ketuk file untuk menginstal (Pastikan izin *"Install from Unknown Sources"* aktif).

### Cara Menggunakan
1.  Siapkan bola basket merek **Spalding** (atau gunakan foto marker yang ada di folder [`/assets`](./assets)).
2.  Buka aplikasi yang sudah diinstal.
3.  Izinkan akses **Kamera** saat diminta.
4.  Arahkan kamera HP ke logo **"SPALDING NBA"** pada bola.
5.  Tunggu sejenak hingga kotak/bola 3D muncul menutupi bola asli.

## 🔧 Troubleshooting (Kendala & Solusi)
Berikut adalah tantangan teknis yang dihadapi selama pengembangan dan solusinya:

* **Masalah:** Objek 3D muncul berwarna abu-abu polos.
    * **Solusi:** Melakukan *Extract Materials* dan *Extract Textures* pada Inspector Unity, atau memasang tekstur `.jpg` secara manual ke prefab.
* **Masalah:** *Duplicate Camera* membuat layar hitam.
    * **Solusi:** Menghapus *Main Camera* bawaan scene dan hanya menggunakan kamera dari *XR Origin*.
* **Masalah:** Marker susah terdeteksi di permukaan bola bulat.
    * **Solusi:** Melakukan *cropping* pada foto marker untuk menghilangkan latar belakang (lantai/tangan) dan fokus pada kontras logo teks.

## 👨‍💻 Tim Pengembang
* **[Nama Lengkap Kamu]** - *NIM* (Role: Developer & AR Logic)
* **[Nama Anggota 2]** - *NIM* (Role: UI/UX & Documentation)
* *(Silakan tambah/edit sesuai anggota kelompok)*

---
*Dibuat dengan ❤️ menggunakan Unity untuk Tugas UAS.*
