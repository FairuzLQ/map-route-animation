# Map Route Animation

Tool web sederhana buat bikin **animasi rute point-to-point** di atas peta asli — mirip AnimateMyMap, tapi gratis, tanpa API key, dan jalan langsung di browser (satu file HTML).

Dibangun pakai **MapLibre GL JS** + basemap raster gratis (CARTO / OSM / Esri / OpenTopoMap) + **OSRM** buat routing jalan asli.

**▶️ Coba langsung: https://fairuzlq.github.io/map-route-animation/**

![preview](preview.png)

## Fitur

- 🗺️ **Peta jalan asli** — 6 tekstur: Voyager, Light, Dark, Satellite, OSM, Topo (tinggal pilih, ganti instan)
- 🏙️ **Gedung 3D** opsional (kelihatan pas peta dimiringkan) — bikin view kota kayak sinematik
- 🔍 **Cari tempat** langsung dari nama (geocoding OpenStreetMap) — gak perlu buka Google Maps
- 📍 **Tambah titik** — cari, paste **link Google Maps** (nama + koordinat auto), ketik `Nama, lat, lng`, atau klik peta
- ↕️ **Urutkan ulang** titik dengan drag-and-drop · **⇅ Balik arah** buat reverse
- 🚗 **Pilih kendaraan** — semua pakai **model 3D** (Three.js): Motor 🏍️, Mobil 🚗, Kereta 🚆, Pesawat ✈️
  - Ban muter, ngadep + belok mulus ngikutin rute; pesawat terbang di ketinggian
  - Tiap kendaraan punya **kecepatan sendiri**: pesawat ngebut buat jarak jauh antar negara/pulau, mobil santai buat lokal
- 🎨 **Warna rute** bisa diganti sesuka hati
- 🎬 **Gaya animasi** — Follow · Cinematic 3D (kamera miring + muter) · Overview
- 🎚️ Atur kecepatan, zoom, dan kemiringan (pitch) kamera
- 💾 **Auto-save** — titik & setting kesimpen otomatis, gak hilang pas refresh
- 🔗 **Share link** — rute dibungkus jadi URL, tinggal kirim ke orang
- 📏 **Total jarak** rute ditampilkan
- ⏺️ **Record ke video** (WebM/MP4) langsung dari browser — tanpa server render
- ⏹️ Batalin animasi kapan aja
- 📱 **Responsive** — di HP panel jadi bottom-sheet yang bisa buka/tutup, peta tetap full-screen
- ✨ Tombol **Contoh** — sekali klik langsung ada rute jadi buat nyoba

## Cara pakai

1. Buka [live demo](https://fairuzlq.github.io/map-route-animation/), atau `index.html` lokal (paling stabil di **Google Chrome**).
2. Paste koordinat / link Google Maps → **Tambah dari teks** (atau klik peta).
3. Titik muncul di **Daftar titik** → drag **⠿** buat urutkan, **✕** buat hapus.
4. Pilih kendaraan, tekstur peta, dan gaya animasi.
5. **▶ Play**. Mau download video? Klik **● Record** dulu → **Play** → **■ Stop & Save**.

### Ambil koordinat dari Google Maps
Buka lokasi di Google Maps → klik kanan → koordinat muncul, tinggal copy. Atau copy URL panjang lokasi (yang ada `@lat,lng` dan `!3d!4d`) — tool-nya ekstrak sendiri.

## Catatan

- Routing "ikut jalan asli" pakai server demo publik OSRM (kadang lambat/rate-limit). Kalau gagal, otomatis fallback ke garis lurus.
- Semua data peta gratis & open. Kredit: © OpenStreetMap, © CARTO, Esri, OpenTopoMap.

## Teknologi

Vanilla HTML/JS — [MapLibre GL JS](https://maplibre.org/), [Turf.js](https://turfjs.org/), [OSRM](http://project-osrm.org/), [OpenFreeMap fonts](https://openfreemap.org/).

## Lisensi

MIT
