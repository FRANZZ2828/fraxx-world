# FRAXX WORLD — Android Mobile Prototype

FRAXX WORLD adalah prototipe aplikasi sandbox 3D yang terinspirasi oleh pola aplikasi game creation mobile. Ini bukan salinan aset, merek, atau kode Roblox/ShinpoBlox.

## Fitur yang sudah berjalan
- Halaman masuk/daftar demo (nama pengguna lokal; belum ada autentikasi server).
- Beranda, Jelajahi, Inventaris, Pesan, Profil, Notifikasi, dan Pelajari.
- Studio 3D Three.js: baseplate, avatar sederhana, kamera sentuh, tambah kubus/bola/silinder/lantai, pilih objek, ubah warna, perbesar/perkecil, hapus.
- Simpan dan muat proyek menggunakan localStorage browser.
- PWA manifest dan service worker dasar untuk pemasangan dari browser Android.

## Jalankan di VS Code
1. Ekstrak ZIP ini.
2. Buka folder `FRAXX-WORLD` di VS Code.
3. Pastikan Node.js versi LTS terpasang.
4. Buka Terminal VS Code pada folder proyek.
5. Jalankan:

   ```bash
   npm install
   npm run dev
   ```
6. Buka alamat lokal yang ditampilkan Vite, biasanya `http://localhost:5173`.

## Tes di HP Android
- Laptop dan HP harus tersambung ke Wi-Fi yang sama.
- Jalankan `npm run dev -- --host 0.0.0.0`.
- Buka alamat Network yang ditampilkan Vite dari Chrome Android, misalnya `http://192.168.x.x:5173`.
- Untuk instalasi PWA, deploy ke hosting HTTPS lalu buka situs di Chrome Android dan pilih **Tambahkan ke layar utama**.

## File penting untuk diubah
- `src/main.js` — halaman, navigasi, login demo, aksi editor dan logika Three.js.
- `src/style.css` — seluruh warna, ukuran, dan tampilan.
- `public/icons/icon.svg` — ikon aplikasi.
- `index.html` — judul dan metadata aplikasi.
- `manifest.webmanifest` — nama aplikasi dan pengaturan PWA.

## Batasan versi ini
- Login/daftar hanya demo lokal, bukan akun online aman.
- Simpan proyek hanya di browser/perangkat yang sama.
- Jelajahi, pesan, notifikasi, dan publikasi online masih berupa kerangka UI; butuh backend/API dan database untuk multi-pengguna.
- Fisika, scripting game, avatar kustom, multiplayer real-time, moderasi, dan sistem publikasi belum termasuk.
- PWA berjalan di Android melalui browser; ini belum APK native. Untuk APK, proyek perlu dibungkus dengan Capacitor dan diuji di Android Studio.

Jangan gunakan data akun atau password penting di prototipe ini.
