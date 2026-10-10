# Jejak NTT — Kuis Sejarah Interaktif

Proyek ini dibuat untuk studi kasus nomor 10 pada Tabel 6 LKM Multimedia WPIF-4139: **Authoring Tools dan Pemrograman** — aplikasi kuis interaktif dan gamifikasi pembelajaran sejarah NTT berbasis scripting.

## Isi folder
- `index.html` — halaman dan struktur hypermedia.
- `css/style.css` — gaya responsif, layout dan aksesibilitas.
- `js/app.js` — logika kuis, penilaian, penyesuaian tingkat kesulitan, penyimpanan lokal dan saran belajar.
- `data/content.js` — 10 topik, garis waktu dan 15 soal dengan pembahasan serta sumber.
- `manifest.webmanifest` — metadata PWA.
- `sw.js` — cache aset untuk akses luring.
- `Laporan_Proyek_Jejak_NTT.docx` — draf laporan akademik yang perlu dilengkapi identitas kelompok dan hasil pengujian nyata.

## Cara menjalankan
1. Ekstrak ZIP.
2. Jalankan server lokal dari folder ini, misalnya dengan Python: `python -m http.server 8000`
3. Buka `http://localhost:8000` pada peramban.
4. Buka sekali dengan koneksi lokal aktif agar service worker menyimpan aset. Setelah itu uji melalui DevTools > Network > Offline.
5. Untuk hosting, unggah seluruh isi folder ke GitHub Pages, Netlify, atau Cloudflare Pages (HTTPS diperlukan untuk service worker).

> Jangan membuka `index.html` dengan `file://` jika ingin menguji PWA/offline; service worker memerlukan HTTPS atau localhost.

## Implementasi Conversational AI dan Generative UI
Asisten belajar menggunakan mesin aturan lokal, bukan API AI daring. Jawaban benar berturut-turut menaikkan level; jawaban salah menurunkannya dan menyimpan topik yang perlu dipelajari. Setelah kuis, rekomendasi belajar dibuat dari skor dan topik yang salah. UI soal, indikator level, progres, pembahasan, hasil dan papan skor dibangun saat runtime berdasarkan state.

## Catatan akademik dan pengujian
- Materi merupakan pengantar, bukan pengganti verifikasi sejarawan/arsip primer. Periksa ulang setiap klaim sebelum publikasi.
- Tautan sumber ada di bagian Tentang situs dan pada pembahasan soal.
- SUS belum boleh diisi dengan data buatan. Uji 10–15 responden sasaran, minta persetujuan, lakukan 3–5 tugas, lalu hitung SUS sesuai LKM.
- Tambahkan nama/NIM anggota, pembagian peran, logbook, tangkapan layar uji, hasil Lighthouse, URL repositori dan URL hosting sebelum pengumpulan.
- Penggunaan bantuan AI generatif wajib dinyatakan terbuka pada laporan sesuai ketentuan LKM.

## Atribusi
Antarmuka, kode dan ilustrasi abstrak dibuat khusus untuk proyek ini. Materi sejarah diringkas/parafrasa dari sumber yang dicantumkan di situs. Tidak ada foto pihak ketiga yang disertakan.
