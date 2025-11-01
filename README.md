# 🏫 Smart Data Parser V2.0 (Dart / Flutter)

**Versi:** 2.0  
**Bahasa:** Dart (Flutter)  
**Platform:** Android, iOS, Desktop (Flutter)  
**Tanggal Rilis:** 2025-11-01

---

## 🌟 Deskripsi Singkat
**Smart Data Parser V2.0** adalah aplikasi **Flutter** untuk mengelola data siswa dengan cara **otomatis dan manual**, menampilkan data dalam **hierarki sekolah → jurusan → kelas → siswa**, lengkap dengan statistik dan animasi UI modern.

Aplikasi ini ideal untuk **administrasi sekolah**, **manajemen data kelas**, dan **pembuatan laporan cepat**.

---

## 🚀 Fitur Utama

| Fitur | Deskripsi |
|-------|-----------|
| 📝 **Input Otomatis** | Parsing teks siswa: `Rina Safitri kelas 11 PPLG` |
| ✍️ **Input Manual** | Form dengan Nama, Sekolah, Jurusan, Kelas |
| 🏫 **Hierarki Data** | ExpansionTile bertingkat: Sekolah → Jurusan → Kelas → Siswa |
| 📊 **Statistik Real-time** | Total siswa, jumlah per sekolah, update otomatis |
| 💾 **Penyimpanan Lokal** | File JSON di `ApplicationDocumentsDirectory` |
| 🎨 **UI Animasi Modern** | Fade, Slide, dan tombol rotasi saat input otomatis |
| 🔍 **Pencarian Cepat** | Filter berdasarkan nama atau jurusan |

---

## 🛠 Teknologi & Library
- Flutter 3.x  
- Dart 3.x  
- `google_fonts` → Font modern (Poppins)  
- `path_provider` → Penyimpanan lokal  
- `dart:convert` → Serialisasi JSON  

---

## 🎯 Cara Menggunakan
2. Tekan **FAB Proses Otomatis** (tombol berputar saat memproses).  
3. Siswa otomatis ditambahkan ke tabel hierarki.

### 2️⃣ Input Manual
1. Isi `Nama`, pilih `Sekolah`, `Jurusan`, dan `Kelas`.  
2. Tekan tombol **Tambah Manual**.  
3. Data muncul langsung di tabel hierarki.

### 3️⃣ Aksi Lain
- **💾 Simpan** → Menyimpan data ke file lokal.  
- **🔄 Segarkan** → Memuat ulang data dari file lokal.  
- **🗑 Hapus Semua** → Menghapus semua data setelah konfirmasi.

---

## 📂 Struktur Data

```dart
class Student {
  String nama;
  String kelas;    // 10, 11, 12
  String jurusan;  // Contoh: PPLG, AKL, FKK
  String sekolah;  // SMK Airlangga / SMK Kesehatan Airlangga
}

### 1️⃣ Input Otomatis
1. Masukkan teks seperti:  
