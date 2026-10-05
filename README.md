# E-Budak | Kindergarten Baitul Taik

Sistem pengurusan murid (PWA) — login parent guna No KB, login guru guna kata laluan.

## Fail dalam repo ni
- `index.html` — aplikasi penuh (HTML + CSS + JS, semua dalam satu fail)
- `manifest.json` — konfigurasi PWA (nama app, ikon, warna tema)
- `sw.js` — service worker untuk sokongan offline
- `icon-192.png`, `icon-512.png` — ikon app

## Cara host guna GitHub Pages (percuma)
1. Buat repo baru di GitHub (contoh: `e-budak`)
2. Upload **semua fail** dalam repo ni terus ke root repo (jangan letak dalam subfolder)
3. Pergi ke **Settings → Pages**
4. Bawah "Source", pilih branch `main` dan folder `/ (root)`
5. Klik **Save** — GitHub akan bagi link macam:
   `https://<username>.github.io/e-budak/`
6. Tunggu 1-2 minit, lepas tu buka link tu — app dah live!

## Cara convert ke Android/iOS app
Bila dah ada link GitHub Pages di atas, boleh guna:
- **median.co** — paste link, generate APK/IPA terus
- **PWA install terus** — buka link kat Chrome (Android) atau Safari (iOS), pilih "Add to Home Screen" — app akan install macam app biasa tanpa perlu Play Store

## Scan Kehadiran (QR)
- Pergi **Kad QR Murid** (menu guru) → pilih kelas → klik **Cetak Semua Kad** → gunting dan agihkan kad kepada murid/letak kat pintu kelas.
- Pergi **Scan Kehadiran (QR)** → klik **Mula Scan** → hala kamera ke kad QR murid → sistem automatik tandakan "Hadir" dan rekod masa check-in.
- Perlukan **kebenaran kamera** (klik "Allow" bila diminta) dan mesti dibuka melalui **HTTPS** (GitHub Pages dah HTTPS by default, jadi ok).
- Kalau kamera/peranti tak sokong scan QR, ada pilihan **masukkan No KB secara manual** sebagai ganti.
- Penjanaan kad QR guna API luar (`api.qrserver.com`) — perlukan internet sekali sahaja untuk papar/cetak kad.

## Nota penting
- Data murid (markah, kehadiran) disimpan dalam **localStorage** peranti — bukan cloud/server. Data akan berbeza antara peranti dan boleh hilang jika cache/app di-uninstall.
- Kata laluan guru default: `guru123` (boleh tukar dalam Tetapan selepas log masuk)
