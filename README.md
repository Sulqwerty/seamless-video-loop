# Seamless Video Loop Creator

Aplikasi web berbasis HTML untuk membuat visualisasi audio dan video loop yang seamless. Aplikasi berjalan di browser dan tidak memerlukan proses build.

## Fitur

- Memuat audio untuk playback dan visualisasi spektrum.
- Mengatur overlay gambar, logo, teks, judul, dan subtitle.
- Menggunakan font lokal atau Google Fonts.
- Memuat gambar atau video sebagai background.
- Mengekspor hasil canvas ke video MP4 jika browser mendukung encoder yang diperlukan.
- Menyimpan dan memuat konfigurasi aplikasi dalam file JSON.

## Menjalankan secara lokal

Jalankan server web sederhana dari folder proyek:

```bash
python -m http.server 8000
```

Kemudian buka <http://localhost:8000>.

## Publikasi dengan GitHub Pages

1. Letakkan `index.html` di root repository.
2. Buka **Settings → Pages** pada repository GitHub.
3. Pilih **Deploy from a branch**, pilih branch yang diinginkan dan folder **/(root)**, lalu simpan.
4. Buka alamat GitHub Pages yang ditampilkan setelah deployment selesai.

## Catatan

Aplikasi ini memuat Tailwind CSS, Font Awesome, Google Fonts, dan Mediabunny dari CDN. Koneksi internet diperlukan untuk memuat library dan font tersebut. Kemampuan ekspor MP4 bergantung pada dukungan browser untuk encoding video H.264 dan audio AAC.
