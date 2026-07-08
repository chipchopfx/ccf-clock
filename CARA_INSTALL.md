# CcF Clock — Web App untuk iPhone XS Max

## Cara Install di iPhone (Add to Home Screen)

### Langkah 1: Upload file ke hosting

Pilih salah satu cara **gratis**:

**Opsi A — GitHub Pages (paling mudah, permanen, HTTPS otomatis)**
1. Buat akun di github.com (jika belum punya)
2. Buat repository baru → nama bebas, misal `ccf-clock`
3. Upload `index.html` dan `manifest.json`
4. Settings → Pages → Source: main branch
5. URL app kamu: `https://[username].github.io/ccf-clock/`

**Opsi B — Netlify Drop (paling cepat, drag & drop)**
1. Buka app.netlify.com/drop
2. Drag & drop folder `CcFClock-web`
3. Netlify langsung beri URL HTTPS — selesai

**Opsi C — Local server di PC/Mac (jika HP dan PC satu jaringan WiFi)**
```bash
# Pastikan Python terinstall, lalu:
cd CcFClock-web
python3 -m http.server 8080
```
Akses dari iPhone: `http://[IP-PC-kamu]:8080` (cari IP PC di network settings)
> ⚠️ Beberapa fitur (Wake Lock, Geolocation) butuh HTTPS — gunakan Opsi A atau B untuk full features.

---

### Langkah 2: Buka di Safari iPhone

1. Buka **Safari** (bukan Chrome/Firefox — harus Safari untuk PWA di iOS)
2. Buka URL app kamu
3. Rotasi ke **landscape** (horizontal)

---

### Langkah 3: Add to Home Screen

1. Tap ikon **Share** (kotak dengan panah ke atas) di toolbar Safari
2. Scroll → tap **"Add to Home Screen"**
3. Nama: `CcF Clock` → tap **Add**

Sekarang ada ikon di Home Screen. Saat dibuka → **full screen, tanpa address bar**, persis seperti app native.

---

### Langkah 4: Konfigurasi

Setelah app terbuka, **long-press** atau tap **⚙️** (pojok kanan atas):

#### Weather
1. Daftar gratis di [openweathermap.org/appid](https://openweathermap.org/appid)
2. Copy API Key
3. Paste di Settings → Weather API Key
4. Isi kota fallback (misal: `Jakarta`)

#### Google Calendar
1. Buka [calendar.google.com](https://calendar.google.com) di **desktop**
2. Klik ⚙️ → **Settings**
3. Pilih kalender kamu di sidebar kiri
4. Scroll ke bawah → cari **"Secret address in iCal format"**
5. Klik **tombol copy** → paste URL di Settings → Google Calendar ICS URL

> URL ini berisi token rahasia — langsung bisa dipakai tanpa login.

---

### Langkah 5: Charge Schedule

iPhone XS Max sudah bisa iOS 17 yang punya fitur bawaan:

**Settings → Battery → Charging Optimization → pilih "80% Limit"**

Selesai. iOS otomatis berhenti charge di 80%. Tidak perlu root, tidak perlu app tambahan.

---

## Troubleshooting

| Problem | Solusi |
|---------|--------|
| Layar tetap mati | Buka dari Home Screen (bukan langsung dari Safari). Wake Lock hanya aktif di PWA mode |
| Weather tidak muncul | Cek API key sudah diisi dan akun OpenWeatherMap sudah verified |
| Kalender tidak muncul | Pastikan ICS URL benar — buka URL tersebut di browser dulu untuk verifikasi |
| Jam tidak full screen | Rotate HP ke landscape dulu, lalu Add to Home Screen |
| Baterai tidak tampil (%) | Battery Status API tidak tersedia di iOS Safari — ini normal |

---

*CcF Clock Web — dibuat untuk iPhone XS Max sebagai clock display 24/7*
