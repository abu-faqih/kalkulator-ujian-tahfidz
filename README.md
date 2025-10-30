KALKULATOR PENGUJI — IKHTIBAR & IMTIHAN
=======================================

Deskripsi Singkat:
------------------
Aplikasi berbasis HTML + Bootstrap untuk menghitung kebutuhan penguji pada acara ikhtibar dan imtihan.
Tampilan modern, responsif, mendukung mode gelap, serta dilengkapi tab terpisah (Ikhtibar / Imtihan),
dropdown kriteria waktu per siswa, animasi hasil, serta fitur salin dan cetak hasil.

--------------------------------------------------
FITUR
--------------------------------------------------
1. Dua mode perhitungan:
   - Ikhtibar (50 / 60 menit per siswa)
   - Imtihan (10 / 15 menit per siswa)

2. Input:
   - Jumlah siswa
   - Jumlah hari ujian
   - Jam efektif per hari
   - Kriteria waktu per siswa

3. Rumus perhitungan:
   jumlahPenguji = ceil( (jumlahSiswa × menitPerSiswa) / (jumlahHari × jamEfektif × 60) )

4. Ringkasan dan rincian:
   - Total menit yang dibutuhkan
   - Total jam efektif tersedia
   - Rata-rata siswa per penguji

5. Fitur tambahan:
   - Tema terang dan gelap (dark mode)
   - Tombol: Hitung, Reset, Salin Hasil, Cetak/Ekspor hasil
   - Animasi hasil angka naik bertahap

--------------------------------------------------
TEKNOLOGI YANG DIGUNAKAN
--------------------------------------------------
- HTML5
- CSS3 (Bootstrap 5, Font Awesome, Google Fonts: Inter)
- JavaScript murni (tanpa framework)

--------------------------------------------------
CARA MENJALANKAN
--------------------------------------------------
1. Clone repositori ini:
   git clone https://github.com/<username>/<repo>.git
   cd <repo>

2. Buka file index.html langsung di browser (double click)
   atau jalankan server lokal:
   python -m http.server 8000
   lalu buka http://localhost:8000

3. Isi data pada tab Ikhtibar atau Imtihan:
   - Masukkan jumlah siswa
   - Masukkan jumlah hari ujian
   - Masukkan jam efektif per hari
   - Pilih kriteria siswa
   - Klik tombol "Hitung"

4. Hasil akan muncul di panel kanan lengkap dengan rincian waktu dan jumlah penguji.

--------------------------------------------------
CONTOH PERHITUNGAN
--------------------------------------------------
Contoh kasus:
- Jumlah siswa: 120
- Jumlah hari: 2
- Jam efektif: 6 jam/hari
- Kriteria: 50 menit (Lancar)

Langkah:
- totalMenitSiswa = 120 × 50 = 6000 menit
- totalMenitEfektif = 2 × 6 × 60 = 720 menit
- jumlahPenguji = ceil(6000 / 720) = 9 penguji

Jadi dibutuhkan 9 penguji.

--------------------------------------------------
STRUKTUR FILE
--------------------------------------------------
/
├── index.html       -> Halaman utama aplikasi
├── assets/          -> Folder opsional untuk logo/screenshot
└── README.txt       -> Dokumentasi (file ini)

--------------------------------------------------
KUSTOMISASI CEPAT
--------------------------------------------------
1. Menambah kriteria baru:
   Edit bagian <select> di index.html, tambahkan opsi baru seperti:
   <option value="40">Sangat Lancar — 40 menit / siswa</option>

2. Mengubah warna tema:
   Edit variabel CSS di bagian :root (misalnya --accent-1 dan --accent-2)

3. Mengubah font:
   Ganti link Google Font di bagian <head> dan ubah font-family di CSS.

--------------------------------------------------
DEPLOY KE GITHUB PAGES
--------------------------------------------------
1. Push repositori ke GitHub.
2. Buka menu Settings → Pages.
3. Pilih branch: main dan folder: root (/).
4. Tunggu beberapa menit.
5. Aplikasi akan tersedia di:
   https://<username>.github.io/<repo>/

--------------------------------------------------
CATATAN
--------------------------------------------------
- Semua perhitungan dilakukan di sisi client (browser).
- Tidak perlu koneksi internet setelah halaman terbuka.
- Aman untuk data non-sensitif.
- Untuk penggunaan besar, sesuaikan parameter input sesuai kebijakan lembaga.

--------------------------------------------------
KONTRIBUSI
--------------------------------------------------
Silakan buat issue atau pull request jika:
- Menemukan bug atau kekeliruan perhitungan.
- Ingin menambah fitur baru seperti:
  * Simpan preset data
  * Ekspor ke CSV/Excel
  * Tambah bahasa baru
  * Fitur cetak otomatis

--------------------------------------------------
LISENSI
--------------------------------------------------
Proyek ini menggunakan lisensi MIT.
Artinya bebas digunakan, dimodifikasi, dan dibagikan dengan mencantumkan atribusi.

--------------------------------------------------
KONTAK
--------------------------------------------------
Untuk bantuan atau pengembangan lanjutan,
hubungi pengembang melalui halaman GitHub project atau issue tracker.
