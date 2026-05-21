# ⛏️ JAY Network CLI Miner (Windows RDP Optimized)

Repositori ini berisi skrip CLI Miner untuk The Jay Network yang telah dimodifikasi dan dioptimalkan khusus untuk berjalan di lingkungan **Windows RDP**. Skrip ini menggunakan **Camoufox (Headless Mode)** untuk melakukan otomatisasi bypass proteksi Cloudflare pool secara senyap di latar belakang.

---

## 🚀 Cara Pemasangan Cepat di RDP Baru

Ikuti langkah-langkah di bawah ini secara berurutan pada Command Prompt (CMD) di RDP baru Anda untuk menjalankan miner secara instan.

Langkah 1: Clone Repositori
Buka CMD, lalu masuk ke direktori utama `C:\` dan ambil file skrip dari GitHub Anda:
```cmd
cd C:\
git clone https://github.com/AssetFinger/my-jay-miner.git
cd my-jay-miner

Langkah 2: Instalasi Python Dependencies
Instal seluruh library Python yang dibutuhkan yang terdaftar di dalam requirements.txt:
```cmd
pip install -r requirements.txt

Langkah 3: Instalasi Engine Browser Camoufox
Unduh komponen browser Playwright yang diperlukan oleh Camoufox agar bisa berjalan di latar belakang:
```cmd
playwright install

Langkah 4: Jalankan Mining!
Jalankan perintah di bawah ini untuk mulai menambang. Skrip akan otomatis mengurus token bypass Cloudflare setiap 5 menit tanpa intervensi manual:
```cmd
python jay-miner.py --wallet Ganti_Dengan_Addressmu --threads 4 --auto-token --jay-wallet-browser
