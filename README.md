# layar-ai

Halaman satu file: jam sekarang + hitung mundur ke waktu **peak / off-peak** tarif DeepSeek API.

## Isi

- `index.html` — semuanya di satu file (HTML + CSS + JS, tanpa dependensi atau request eksternal).
- Jam besar, zona waktu bisa diganti: WITA (Manado), UTC, atau zona perangkat.
- Status 🟢 off-peak / 🔴 peak, hitung mundur ke pergantian berikutnya, progress jendela berjalan.
- Peta 24 jam hari ini dengan penanda posisi sekarang.

## Jadwal

| Zona | Peak (Senin–Jumat) | Off-peak |
| --- | --- | --- |
| UTC | 01.00–04.00, 06.00–10.00 | sisanya |
| WITA / Tiongkok (UTC+8) | 09.00–12.00, 14.00–18.00 | sisanya |

Sabtu, Minggu, dan libur nasional Tiongkok = off-peak sepanjang hari.

Jendela peak dipatok UTC di array `PEAK_UTC` pada `index.html`. Libur Tiongkok bisa diisi di array `HOLIDAYS` (format `YYYY-MM-DD`, waktu UTC+8) — kosong secara default karena tanggal resmi perlu dicek dari pengumuman pemerintah Tiongkok.

Sumber: https://deepseek.ai/pricing

## Pakai lokal

Buka `index.html` di browser. Tidak perlu build atau server.

## GitHub Pages

Settings → Pages → Source: *Deploy from a branch* → Branch `main`, folder `/ (root)`.
