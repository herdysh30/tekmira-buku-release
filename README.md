# 📚 Toko Buku tekMIRA

Aplikasi mobile jual-beli buku seputar **energi, mineral, dan batubara** — dikembangkan selama program magang di [tekMIRA](https://www.tekmira.esdm.go.id/) menggunakan **Flutter**.

> [!NOTE]
> **APK yang tersedia di halaman Release adalah versi demo.**
> Aplikasi ini terhubung ke backend & database pribadi (staging) — bukan rilis produksi.
> APK disediakan untuk keperluan demonstrasi portofolio dan review rekruter.

---

## ⚠️ Batasan Versi Demo

Semua fitur di sisi pembeli **berfungsi**, namun beberapa alur bergantung pada aksi admin yang tidak tersedia di versi demo ini:

| Fitur | Status Demo | Keterangan |
|-------|:-----------:|------------|
| Register & Login | ✅ Berfungsi | — |
| Katalog, Pencarian, Filter | ✅ Berfungsi | — |
| Detail Buku & Rekomendasi | ✅ Berfungsi | — |
| Keranjang & Wishlist | ✅ Berfungsi | — |
| Checkout & Hitung Ongkir | ✅ Berfungsi | — |
| Upload Bukti Pembayaran | ✅ Berfungsi | — |
| Verifikasi Mahasiswa | ⚠️ Terbatas | Upload KTM bisa, tetapi approval oleh admin tidak tersedia |
| Status Pesanan | ⚠️ Terbatas | Mentok di **"Menunggu Verifikasi Pembayaran"** — konfirmasi, input resi, dan "Pesanan Selesai" membutuhkan aksi admin |
| Notifikasi Push | ⚠️ Terbatas | Notifikasi hanya dikirim saat admin mengonfirmasi pembayaran atau mengirim resi — tidak akan muncul di demo |
| Ulasan Buku | ❌ Tidak bisa | Ulasan hanya bisa ditulis setelah pesanan berstatus selesai |
| Rekening Pembayaran | ℹ️ Dummy | Nomor rekening di halaman pembayaran adalah **data dummy** (bukan rekening asli instansi) |

---

## ✨ Fitur Lengkap (di versi production)

### 👤 Sisi Pembeli
| Fitur | Keterangan |
|-------|-----------|
| **Autentikasi** | Register, login, logout, lupa password |
| **Katalog Buku** | Pencarian, filter kategori, sorting, pagination |
| **Detail Buku** | Galeri foto, rekomendasi serupa, ulasan pembeli |
| **Keranjang & Wishlist** | Sinkronisasi real-time dengan server |
| **Checkout** | Pilih alamat, hitung ongkir otomatis (Raja Ongkir), diskon |
| **Pembayaran Manual** | Upload bukti transfer |
| **Ulasan** | Tulis, edit, hapus review — termasuk balasan admin |
| **Notifikasi** | Push notification real-time (Firebase Cloud Messaging) |
| **Verifikasi Mahasiswa** | Upload foto KTM untuk verifikasi status mahasiswa |
| **Manajemen Alamat** | CRUD alamat pengiriman + set alamat utama |

### 🛠️ Sisi Admin *(tidak tersedia di demo)*
| Fitur | Keterangan |
|-------|-----------|
| **Dashboard** | KPI ringkas, grafik penjualan bulanan, buku bestseller |
| **Kelola Pesanan** | Lihat, proses, update status pesanan |
| **Kelola Buku** | CRUD buku, kategori, stok |
| **Kelola Diskon** | Buat & atur diskon / voucher |
| **Verifikasi Mahasiswa** | Approve / reject verifikasi KTM |
| **Penjualan Tunai** | Cash sale langsung tanpa pengiriman |

---

## 🛠️ Tech Stack

| Layer | Teknologi |
|-------|-----------|
| **Framework** | Flutter 3.x (Dart) |
| **State Management** | Riverpod |
| **Routing** | Go Router |
| **Networking** | Dio (REST API) |
| **Push Notification** | Firebase Cloud Messaging (FCM) |
| **Ongkos Kirim** | Raja Ongkir API |
| **Arsitektur** | Clean Architecture |
| **Storage** | Flutter Secure Storage, Shared Preferences |
| **Image** | Cached Network Image, Photo View, Image Picker/Cropper |

---

## 📱 Screenshots

<p align="center">
  <img src="https://res.cloudinary.com/fuuxoksh/image/upload/f_auto,q_auto,w_250/Screenshot_1792807188" width="200" alt="Home" />
  &nbsp;&nbsp;
  <img src="https://res.cloudinary.com/fuuxoksh/image/upload/f_auto,q_auto,w_250/Screenshot_1792807533" width="200" alt="Catalog" />
  &nbsp;&nbsp;
  <img src="https://res.cloudinary.com/fuuxoksh/image/upload/f_auto,q_auto,w_250/Screenshot_1792807540" width="200" alt="Detail" />
</p>

---

## 📥 Download Demo APK

Unduh APK demo dari halaman **[Releases](../../releases/tag/v1.0.0)**.

> [!WARNING]
> Ini adalah APK **demo** yang terhubung ke backend staging pribadi.
> Beberapa alur terbatas karena membutuhkan aksi admin — lihat tabel batasan di atas.

---

## 📋 Informasi Project

| | |
|---|---|
| **Dikembangkan** | Sep 2025 – Okt 2025 |
| **Konteks** | Program Magang — tekMIRA (Pusat Riset dan Teknologi Mineral dan Batubara) |
| **Role** | Mobile Developer |
| **Source Code** | Private (kode milik instansi) |

---

## 📄 Lisensi

Source code bersifat **proprietary** — hak cipta milik tekMIRA.
APK demo yang dirilis di repository ini hanya untuk keperluan demonstrasi portofolio.
