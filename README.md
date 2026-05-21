# ⛏️ JAY Network CLI Miner (Windows RDP Optimized)

Repositori ini berisi skrip CLI Miner untuk The Jay Network yang telah dimodifikasi dan dioptimalkan khusus untuk berjalan di lingkungan **Windows RDP**. Skrip ini menggunakan **Camoufox (Headless Mode)** untuk melakukan otomatisasi bypass proteksi Cloudflare pool secara senyap di latar belakang.

---

## 🚀 Cara Pemasangan Cepat di RDP Baru

Ikuti langkah-langkah di bawah ini secara berurutan pada Command Prompt (CMD) di RDP baru Anda untuk menjalankan miner secara instan.

### Langkah 1: Clone Repositori
Buka CMD, lalu masuk ke direktori utama `C:\` dan ambil file skrip dari GitHub Anda:
```cmd
cd C:\
git clone [https://github.com/AssetFinger/my-jay-miner.git](https://github.com/AssetFinger/my-jay-miner.git)
cd my-jay-miner

```

### Langkah 2: Instalasi Python Dependencies

Instal seluruh library Python yang dibutuhkan yang terdaftar di dalam `requirements.txt`:

```cmd
pip install -r requirements.txt

```

### Langkah 3: Instalasi Engine Browser Camoufox

Unduh komponen browser Playwright yang diperlukan oleh Camoufox agar bisa berjalan di latar belakang:

```cmd
playwright install

```

### Langkah 4: Jalankan Mining!

Jalankan perintah di bawah ini untuk mulai menambang. Skrip akan otomatis mengurus token bypass Cloudflare setiap 5 menit tanpa intervensi manual:

```cmd
python jay-miner.py --wallet Ganti_Dengan_Addressmu --threads 4 --auto-token --jay-wallet-browser

```

---

## 🛠️ Ringkasan Modifikasi Windows RDP

Skrip `jay-miner.py` di dalam repositori ini telah disesuaikan dari versi Linux aslinya dengan perubahan berikut:

1. **Bypass Xvfb Linux:** Fungsi `_ensure_xvfb` telah dimatikan (`pass`) karena Windows RDP tidak menggunakan virtual display server Linux.
2. **Camoufox Headless Mode:** Pengaturan browser diubah menjadi `headless=True` agar berjalan senyap di memori RDP, menghindari crash grafis akibat pembatasan hak akses Administrator RDP.

---

## 📊 Parameter Perintah (Arguments)

Jika Anda ingin menyesuaikan performa mining, Anda bisa mengubah beberapa parameter berikut pada perintah jalankan:

* `--wallet` / `-w` : Alamat wallet JAY Anda (Wajib).
* `--threads` / `-t` : Jumlah core CPU yang dialokasikan (Contoh: `--threads 4` atau `--threads 8`).
* `--auto-token` : Memaksa skrip menggunakan modul otomatisasi Camoufox (Direkomendasikan).
* `--verbose` / `-v` : Memunculkan log detail koneksi pool dan job secara lengkap di CMD.

```
