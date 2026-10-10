# Majalah Sekolah — prototipe tahap 1

Prototipe frontend React berdasarkan struktur visual `Karya Siswa.pdf`: halaman tulisan, kategori, arsip majalah, dan formulir kirim karya.

## Menjalankan di komputer

1. Instal Node.js versi LTS dari https://nodejs.org/
2. Ekstrak folder proyek.
3. Buka terminal di folder `majalah-sekolah`.
4. Jalankan:

   ```bash
   npm install
   npm run dev
   ```

5. Buka alamat lokal yang ditampilkan Vite di terminal.

Untuk membuat versi produksi:

```bash
npm run build
```

## Yang sudah tersedia

- Layout responsif desktop dan HP.
- Kartu artikel contoh dan filter kategori.
- Pencarian judul/sekolah.
- Tampilan sampul arsip majalah contoh.
- Formulir kontribusi yang melakukan validasi dasar.
- Status karya baru `pending` di state React selama sesi prototipe.

## Batasan yang perlu diketahui

Ini baru frontend/prototipe. Artikel contoh bukan publikasi nyata. Formulir belum mengirim data ke server, tidak menyimpan data secara permanen, belum ada login/otorisasi admin, belum ada unggah gambar sesungguhnya, dan belum ada database.

## Tahap backend berikutnya

Sambungkan Supabase dengan tabel `schools`, `school_members`, `magazines`, `magazine_issues`, `articles`, dan `article_images`. Terapkan autentikasi, Row Level Security (RLS), kebijakan akses berdasarkan sekolah, penyimpanan foto, serta status artikel `draft`, `pending`, `published`, dan `rejected`. Jangan menyimpan service-role key di kode frontend. Semua keputusan publikasi harus diperiksa oleh backend, bukan hanya disembunyikan di UI.

