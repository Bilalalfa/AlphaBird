# Alpha Flap - Flappy Bird Cyberpunk Clone

Game bergaya retro-arcade Cyberpunk berbasis browser yang terinspirasi dari Flappy Bird klasik. Game ini dikembangkan menggunakan teknologi web murni tanpa pustaka eksternal yang berat.

## 🛠️ Teknologi & Framework yang Digunakan

Projek ini **tidak menggunakan framework JavaScript** (seperti React, Vue, Angular) atau framework game (seperti Phaser, PixiJS, Three.js). Game ini sepenuhnya dibangun menggunakan **Vanilla Web Stack**:

1. **HTML5**:
   - Struktur halaman dasar.
   - Elemen `<canvas>` sebagai area rendering game secara visual.
2. **Vanilla CSS3**:
   - Desain antarmuka (UI) bernuansa *Cyberpunk* dan *Arcade* menggunakan variabel CSS (`:root`), efek *glassmorphism*, neon *glow*, animasi halus (`@keyframes`), dan *layout flexbox/grid*.
   - Responsif secara penuh untuk perangkat mobile dan desktop.
3. **Vanilla JavaScript (ES6+)**:
   - **Canvas 2D Context API**: Untuk merender semua grafis secara dinamis (burung, pipa rintangan, latar belakang paralaks kota, partikel ledakan, bintang berkelap-kelip, dan efek getaran layar *camera shake*).
   - **Web Audio API**: Digunakan untuk mensintesis (membuat) efek suara *synthesizer* retro secara langsung via kode (programmatic audio) tanpa perlu memuat file audio eksternal (`.mp3` atau `.wav`).
   - **Game Loop**: Menggunakan `requestAnimationFrame` dengan pendekatan delta-time/accumulator untuk menjamin gameplay yang konsisten pada layar dengan refresh rate tinggi (60Hz, 120Hz, dst.).
   - **Local Storage API**: Menyimpan data skor terbaik (*high score*) dan pengaturan suara mute secara permanen di browser pemain.
4. **Pustaka Eksternal (via CDN)**:
   - **FontAwesome (v6.4.0)**: Untuk ikon dashboard, suara, medali, dan kontrol.
   - **Google Fonts**: Font `Outfit` untuk teks modern/UI dan `Press Start 2P` untuk teks piksel bergaya retro-arcade.

---

## 🕹️ Fitur Utama

- **Latar Belakang Paralaks**: Efek kota cyberpunk berlapis-lapis dan bintang berkelap-kelip yang bergerak dengan kecepatan berbeda untuk menciptakan kedalaman visual 3D semu.
- **Sintesis Audio Retro (Web Audio API)**: Suara lompatan, skor, dan kehancuran dihasilkan secara dinamis oleh generator gelombang audio segitiga dan persegi.
- **Sistem Medali & Rekor**: Mendapatkan medali (Perunggu, Perak, Emas, Platinum) berdasarkan pencapaian skor dan menampilkan lencana "Rekor Baru!" saat skor tertinggi terpecahkan.
- **Efek Partikel & Layar Bergetar (Camera Shake)**: Partikel neon muncul saat burung melompat atau menabrak rintangan, ditambah efek layar bergetar saat game over untuk menambah kepuasan bermain.

---

## ⚙️ Persyaratan Sistem & Cara Menjalankan

### Persyaratan Sistem:
- **Peramban Web (Browser)** modern seperti Google Chrome, Mozilla Firefox, Microsoft Edge, atau Safari.
- Koneksi internet (hanya saat pertama kali membuka untuk memuat Font & Ikon dari CDN).

### Cara Menjalankan Game:

#### Cara 1: Buka Langsung (Tanpa Instalasi)
1. Cari berkas [index.html](file:///d:/finish/New%20folder/Kuliah/AlphaBird/index.html) di folder projek Anda.
2. Klik dua kali (atau klik kanan dan pilih **Open With** browser kesayangan Anda).
3. Game siap dimainkan!

#### Cara 2: Menggunakan Local Web Server (Direkomendasikan)
Untuk mencegah batasan kebijakan keamanan lokal browser pada beberapa fitur modern (seperti Local Storage atau Audio Context pada beberapa kondisi browser tertentu), disarankan menggunakan server lokal kecil:
- **VS Code**: Pasang ekstensi **Live Server**, lalu klik tombol *Go Live* di kanan bawah editor.
- **Node.js**:
  ```bash
  npx http-server .
  ```
  Lalu buka alamat `http://localhost:8080` di browser Anda.
- **Python**:
  ```bash
  python -m http.server 8000
  ```
  Lahu buka alamat `http://localhost:8000` di browser Anda.

---

## ⌨️ Kontrol Game

| Kontrol | Keyboard | Touchscreen (HP) |
| --- | --- | --- |
| **Melompat / Terbang** | `SPASI` | Ketuk Layar |
| **Mulai / Main Lagi** | `SPASI` / `Enter` | Ketuk tombol "Main Lagi" |
| **Mute / Unmute Suara** | Klik Ikon Speaker | Ketuk Ikon Speaker |
