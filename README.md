# 📚 Toko Buku tekMIRA

Aplikasi mobile jual-beli buku seputar **energi, mineral, dan batubara** — dikembangkan selama program magang di [tekMIRA](https://www.tekmira.esdm.go.id/) menggunakan **Flutter**.

> [!NOTE]
> **APK yang tersedia di halaman Release adalah versi demo.**
> Aplikasi ini terhubung ke backend & database pribadi (staging) — bukan rilis produksi.
> APK disediakan untuk keperluan demonstrasi portofolio dan review rekruter.

---

## ⚠️ Batasan Demo

Semua fitur di sisi pembeli **berfungsi penuh**, termasuk register/login, jelajah katalog, pencarian, filter, wishlist, keranjang belanja, manajemen alamat, checkout dengan hitung ongkir (Raja Ongkir), upload bukti pembayaran, dan upload KTM.

**Namun**, karena **akun/dashboard admin tidak di-expose** di versi demo ini, beberapa alur lanjutan memiliki batasan:

1. **Alur Pesanan Mentok di Verifikasi Pembayaran**
   Setelah upload bukti transfer, status pesanan akan berhenti di **"Menunggu Verifikasi Pembayaran oleh Admin"** — tidak sampai tahap input resi pengiriman maupun **"Pesanan Selesai"**.
2. **Verifikasi Mahasiswa Hanya Sampai Upload**
   Pengguna dapat mengunggah foto KTM, namun persetujuan (ACC) status mahasiswa harus dilakukan oleh admin.
3. **Notifikasi Push Tidak Terpicu**
   Notifikasi FCM hanya dikirim saat admin memverifikasi pembayaran atau mengirimkan nomor resi, sehingga tidak akan muncul selama penggunaan demo.
4. **Ulasan Buku Tidak Dapat Dikirim**
   Fitur tulis ulasan hanya terbuka setelah pesanan berstatus selesai, sehingga pada versi demo tidak dapat dicoba hingga submit.
5. **Rekening Pembayaran Dummy**
   Data rekening pada kartu instruksi pembayaran telah diganti menjadi data dummy (`Bank Demo (Simulasi)` — `000-000000000-0` a.n. `TekMIRA Demo Store`) demi keamanan data instansi.

---

## ✨ Fitur Utama

### 👤 Sisi Pembeli
| Fitur | Keterangan |
|-------|-----------|
| **Autentikasi** | Register, login, logout, lupa password |
| **Katalog Buku** | Pencarian, filter kategori, sorting, pagination |
| **Detail Buku** | Galeri foto, rekomendasi serupa, ulasan pembeli |
| **Keranjang & Wishlist** | Sinkronisasi real-time dengan server |
| **Checkout** | Pilih alamat, hitung ongkir otomatis (Raja Ongkir), diskon |
| **Pembayaran Manual** | Upload bukti transfer (rekening dummy di versi demo) |
| **Ulasan** | Tulis, edit, hapus review — termasuk balasan admin *(butuh pesanan selesai)* |
| **Notifikasi** | Push notification real-time (Firebase Cloud Messaging) *(terpicu oleh aksi admin)* |
| **Verifikasi Mahasiswa** | Upload foto KTM untuk verifikasi status mahasiswa |
| **Manajemen Alamat** | CRUD alamat pengiriman + set alamat utama |

### 🛠️ Sisi Admin *(tidak tersedia di demo)*
| Fitur | Keterangan |
|-------|-----------|
| **Dashboard** | KPI ringkas, grafik penjualan bulanan, buku bestseller |
| **Kelola Pesanan** | Verifikasi pembayaran, input resi, update status pesanan |
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
> Seluruh fitur pembeli berjalan, namun alur yang membutuhkan persetujuan admin (verifikasi pembayaran, input resi, verifikasi KTM, notifikasi, serta penulisan ulasan) tidak dapat diselesaikan karena dashboard admin tidak di-expose.

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
