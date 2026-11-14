# 🏕️ Mendoventura - Sistem Penyewaan Alat Camping Berbasis Objek

Mendoventura adalah sistem informasi manajemen penyewaan perlengkapan kegiatan outdoor yang dirancang menggunakan paradigma Pemrograman Berorientasi Objek (PBO). Sistem ini mendigitalisasi proses bisnis rental alat camping untuk mengatasi masalah *double booking*, ketidakakuratan stok, serta mempermudah penelusuran kerusakan atau kehilangan alat.

---

## 👥 Tim Pengembang (Kelompok 4 - Mendoan Racing)
* **Nabilla Dwi Putri Paraswati** (2505060059) - Ketua / Manajer Proyek & Analis Kebutuhan
* **Excel Bagus Herlambang** (2505060056) - Perancang Kelas CRC & Class Diagram
* **Zuyina M. Irkham** (2505060041) - Pengembang Kerangka Kode & Repositori GitHub
* **Aufa Abid Rahman Nashir** (2505060055) - Penguji & Dokumentasi

**Dosen Pengampu:** Imam Adi Nata, M.Kom.

---

## 🚀 Fitur Utama & Kebutuhan Fungsional
Sistem ini memisahkan hak akses berdasarkan 3 Aktor utama (Pelanggan, Admin, Pemilik) dengan fungsionalitas berikut:

* **Pelanggan:** Melihat katalog terfilter per tanggal, registrasi/login, melakukan reservasi multi-alat, serta mengunggah bukti bayar & kartu identitas.
* **Admin:** Memverifikasi pesanan/pembayaran, mengubah status sewa, mencatat kondisi alat saat keluar/masuk, dan menginput denda keterlambatan/kerusakan.
* **Pemilik:** Memantau laporan penyewaan (bulanan/tahunan) serta laporan pendapatan sewa & denda.
* **Sistem (Otomatis):** Memeriksa ketersediaan stok per tanggal secara terpusat untuk menolak bentrok jadwal dan menghitung biaya sewa/denda otomatis.

---

## 🏗️ Struktur Kelas & Desain PBO (Domain Model)
Kerangka kode proyek ini dirancang berdasarkan seleksi kandidat kelas berikut:
* `Pengguna` (Abstract Class) ➡️ Diturunkan menjadi kelas `Pelanggan`, `Admin`, dan `Pemilik`.
* `Peralatan` (Abstract Class) ➡️ Diturunkan menjadi kelas spesifik: `Tenda`, `Carrier`, `SleepingBag`, dan `Kompor`.
* `Sewa` (Reservasi) & `ItemSewa` ➡️ Mengelola logika transaksi utama dan kuantitas barang.
* `Ketersediaan` ➡️ Kelas khusus pemisah logika agar pengecekan stok terisolasi dengan baik.
* `CekKondisi` ➡️ Mencatat kondisi alat menggunakan enum `Kondisi`.
* `Denda` & `AturanDenda` (Interface) ➡️ Polimorfisme perhitungan denda akibat telat, rusak, atau hilang.
ranch penulisan testing script (Aufa).
*
