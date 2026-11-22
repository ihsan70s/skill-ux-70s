---
name: skill-ux-70s
description: Rancang dan tinjau UX halaman dan alur website dengan shadcn/ui. Tentukan perjalanan pengguna, susunan halaman, arah visual, kondisi layar, dan perilaku responsif untuk kode atau Figma.
---

# Skill UX 70s

Mulai dari tugas pengguna dan aturan produk. Susun komponen shadcn/ui yang sesuai menjadi antarmuka yang jelas dan mudah diakses.

Hasil standar berupa spesifikasi UX. Tambahkan wireframe beranotasi jika diminta atau jika susunan halaman sulit dijelaskan dengan teks. Sesuaikan spesifikasi dengan tujuan pengguna: kode, Figma, atau keduanya. Bila tujuan belum disebutkan, siapkan spesifikasi yang bisa dipakai untuk keduanya. Teruskan pengerjaan ke skill implementasi atau Figma yang sesuai.

## Alur kerja

Sebelum merancang fitur atau halaman baru, periksa apakah brief atau proyek sudah punya PRD yang mencakupnya. Gunakan PRD itu sebagai acuan. Jika belum ada, beri tahu pengguna lewat chat bahwa PRD menjadi hasil pertama, tawarkan [prompt siap pakai](references/prd.md), lalu buat draf dari brief yang sudah diberikan. Selesaikan PRD sebagai dokumen terpisah sebelum merancang UX. Untuk halaman kecil, buat tiap bagian tetap ringkas.

1. Tentukan tujuan halaman, peran pengguna, aksi utama, dan batasan. Gunakan panduan bertanya di bawah untuk keputusan yang masih terbuka.
2. Baca `DESIGN.md` bila tersedia sebagai acuan lintas halaman. Cek komponen, token, dan layar terkait. Catat pengecualian per halaman beserta alasannya. Jika ada hasil riset, gunakan untuk memahami tujuan, hambatan, dan cara kerja pengguna. Kaitkan keputusan penting dengan temuan dan tandai asumsi yang bisa mengubah alur.
3. Petakan tugas ke bagian halaman dan langkah pengguna. Tentukan kondisi layar dan aksi berikutnya sebelum menyusun layout.
4. Pakai komponen shadcn/ui yang diberikan pengguna atau tersedia di proyek. Jika belum ada daftar, gunakan katalog shadcn/ui serta [panduan komponen](references/components.md) dan tandai pilihan sebagai usulan. Untuk tiap bagian, tentukan posisi, isi, komponen, varian, dan aksi. Jika daftar tersedia tetapi ada kebutuhan yang belum tercakup, catat usulan untuk serah terima.
5. Tentukan isi, hierarki, dan perilaku komponen untuk kondisi relevan seperti normal, hover, fokus, terpilih, nonaktif, memuat, berhasil, dan gagal. Jelaskan hasil tiap aksi, termasuk validasi, konfirmasi, dan pembatalan.
6. Rancang layout responsif dan aksesibilitas. Jelaskan token proyek untuk permukaan, teks, aksi utama, fokus, dan umpan balik, serta tipografi, jarak, dan pengelompokan. Jika arah visual atau token belum ada, gunakan [pola arah visual](references/visual-direction.md) dan tandai pilihannya sebagai usulan.
7. Tinjau apakah pengguna dapat menemukan aksi, memahami dampaknya, menyelesaikan tugas, dan pulih dari kesalahan. Jika tersedia pratinjau, cek desktop, mobile, keyboard jika didukung, dan kondisi kosong serta gagal yang relevan. Perbaiki temuan dalam cakupan dan cek ulang.

## Keputusan desain lewat chat

- Untuk setiap permintaan merancang form tambah data (create) atau edit data, tanyakan di chat bentuk tampilannya sebelum menetapkan layout, kecuali pengguna sudah menyebut pilihannya. Tawarkan tiga opsi: **Halaman penuh (full page)** untuk tugas panjang, bertahap, atau yang butuh ruang dan URL sendiri, **Modal (Dialog)** untuk isian singkat dan terfokus, serta **Drawer (Sheet atau Drawer)** jika pengguna perlu tetap punya konteks dari halaman asal. Urutkan opsi yang paling sesuai di posisi pertama, beri label **Rekomendasi**, dan tunggu pilihan pengguna. Jika permintaan mencakup tambah dan edit, tanyakan keduanya sekaligus dan izinkan pilihan yang berbeda.
- Tanya langsung bila jawabannya bisa mengubah tujuan, alur utama, atau aturan produk. Untuk detail layout atau visual yang mudah diubah, lanjutkan dengan asumsi yang dicatat.
- Beri dua atau tiga opsi. Letakkan **Rekomendasi** di urutan pertama dan jelaskan alasan singkat serta dampak tiap opsi. Gunakan pilihan yang bisa diklik jika tersedia. Jika tidak, gunakan opsi bernomor.
- Izinkan jawaban sendiri. Gunakan pertanyaan bebas bila nilainya hanya bisa diberikan oleh pengguna, seperti teks yang telah disetujui atau warna merek.
- Tunggu jawaban sebelum memfinalkan keputusan terkait. Lanjutkan bagian yang bisa dikerjakan secara terpisah.

## Kondisi layar dan transisi

- Minta konfirmasi sebelum membuat atau menyimpan data, menerapkan edit, menghapus data, atau menjalankan tindakan lain yang memerlukan persetujuan, seperti publikasi, pengarsipan, dan perubahan massal. Letakkan konfirmasi tepat sebelum data berubah. Untuk formulir, validasi isian sebelum menampilkan `Alert Dialog`. Jika batal, pertahankan data tersimpan beserta draf atau pilihan terkait. Jika disetujui, jalankan aksi dan tampilkan proses serta hasilnya. Ikuti aturan produk yang eksplisit. Tanya lewat chat bila kebutuhan konfirmasi pada tindakan lain belum jelas dan mengubah alur.
- Untuk setiap kondisi penting, catat pemicu, komponen dan pesan yang tampil, aksi yang tersedia, serta kondisi berikutnya. Sertakan transisi otomatis yang relevan, seperti memuat lalu menampilkan konten atau kegagalan.
- Rancang pemulihan. Saat simpan gagal, pertahankan isian, tampilkan pesan spesifik di dekat formulir atau kolom, dan jelaskan hasil percobaan ulang.
- Cek label panjang di layar sempit, angka nol yang perlu dibedakan dari data kosong, dan tampilan pengganti bila gambar gagal dimuat.

### Teks antarmuka

- Tulis usulan teks di kondisi atau interaksi terkait. Gunakan label spesifik seperti **Simpan perubahan** atau **Hapus produk**.
- Untuk konfirmasi, sebutkan tindakan dan data terdampak. Jelaskan konsekuensi jika membantu pengguna memilih, seperti jumlah data, siapa yang bisa melihat publikasi, atau apakah penghapusan bisa dibatalkan. Contoh: **Simpan perubahan profil?**, dengan **Lanjut edit** dan **Simpan perubahan**. Untuk hapus, gunakan **Hapus produk ini?**, dengan **Pertahankan produk** dan **Hapus produk**. Jika simpan juga memublikasikan perubahan, gunakan **Simpan dan publikasikan** dan jelaskan dampaknya.
- Sesuaikan pesan dengan kondisi. Daftar kosong bisa menawarkan **Tambah produk**, sedangkan hasil filter kosong menawarkan **Hapus filter**. Pesan kesalahan menyebut kejadian dan langkah pemulihan. Sebutkan penyebab jika diketahui.
- Letakkan petunjuk dan validasi di dekat kolom terkait. Gunakan tooltip untuk informasi tambahan.
- Gunakan kata yang akrab dan istilah konsisten. Pertahankan fakta, syarat, dan tingkat kepastian saat meringkas. Contoh gagal simpan: **Perubahan belum tersimpan** dengan aksi **Coba lagi**.

## Layout dan perilaku responsif

- Kelompokkan komponen berdasarkan tugas. Dekatkan kontrol terkait dan beri jarak lebih besar antargrup sesuai skala proyek. Gunakan pemisah jika batas grup masih kurang jelas.
- Sejajarkan judul, kontrol, dan konten. Utamakan informasi dan aksi penting serta selaraskan urutan visual, urutan baca, dan fokus keyboard.
- Jelaskan bagian yang turun baris, berpindah ke panel dengan pemicu yang terlihat, atau tetap terlihat saat ruang menyempit. Tentukan perubahan dari ruang yang dibutuhkan konten dan label. Jaga aksi utama tetap terjangkau. Misalnya, pertahankan pencarian dan pindahkan filter tambahan ke `Sheet` yang dibuka lewat tombol **Filter**.

## Pemilihan komponen

- Pilih pola paling sederhana yang memenuhi tugas. Sertakan kontrol dan dekorasi jika mendukung pengguna.
- Tetapkan satu aksi utama di tiap area keputusan. Bedakan aksi destruktif secara visual dan ikuti aturan konfirmasi.
- Pilih input sesuai jenis nilai, seperti teks bebas, satu atau banyak pilihan, tanggal atau waktu, rentang angka, dan pilihan biner. Gunakan label terlihat dan spesifik.
- Gunakan dialog untuk keputusan singkat. Gunakan panel samping atau drawer untuk tugas yang memerlukan lebih banyak konteks. Hindari overlay bertumpuk.
- Gunakan tabel untuk membandingkan data dengan kolom yang konsisten. Siapkan penyajian yang sesuai jika tabel sulit dibaca di layar sempit.
- Gunakan komponen umpan balik untuk status dan progres, dengan penanda lain selain warna.
- Gunakan kontrol buka-tutup dengan label yang jelas untuk informasi sekunder. Pakai breadcrumb, tab, paginasi, atau sidebar jika membantu pengguna mengetahui posisi atau berpindah bagian.

## Interaksi dan aksesibilitas

- Pastikan aksi dapat dioperasikan lewat keyboard. Tentukan indikator fokus yang jelas dan jaga agar kontrol yang mendapat fokus tetap terlihat saat ada header, bilah aksi yang menempel, atau panel yang menutupi sebagian halaman.
- Beri label yang bisa dibaca teknologi bantu pada setiap input. Hubungkan petunjuk dan kesalahan ke kolom terkait.
- Gunakan judul dan penanda wilayah halaman yang semantis. Selaraskan urutan baca dan fokus dengan tampilan.
- Beri nama aksesibel pada semua kontrol, termasuk tombol ikon.
- Saat overlay terbuka, pindahkan dan pertahankan fokus di dalamnya. Saat ditutup, kembalikan fokus ke pemicu.
- Pasangkan warna status dan validasi dengan teks atau pengumuman yang bisa diakses.
- Tentukan pasangan warna untuk teks, latar, dan indikator fokus agar kontrasnya bisa diperiksa pada tiap kondisi dan tema yang dirancang.
- Hormati preferensi pengurangan gerakan dan hindari animasi yang menghambat tugas.
- Tentukan ukuran area tekan dan jarak antarkontrol, terutama untuk tombol ikon yang berdekatan seperti **Edit** dan **Hapus**. Tampilkan aksi penting tanpa bergantung pada hover.
- Jika tugas memakai drag, sediakan aksi yang bisa dijalankan tanpa menyeret dan dapat dioperasikan dengan keyboard, seperti **Pindah ke atas** dan **Pindah ke bawah**.
- Saat validasi gagal, pertahankan isian, jelaskan cara memperbaikinya, dan tentukan tujuan fokus, misalnya ringkasan kesalahan atau kolom pertama yang bermasalah. Dalam formulir bertahap, gunakan kembali data yang sudah diisi jika masih berlaku.

## Tinjauan desain

- Untuk serah terima, catat pemeriksaan aksesibilitas yang masih perlu dilakukan pada halaman yang sudah berjalan, seperti pengukuran kontras dan area tekan, navigasi keyboard, serta pengumuman status dengan pembaca layar.
- Untuk spesifikasi atau wireframe, cek alur utama, struktur halaman, dan kemudahan menemukan aksi. Pada desain rinci, cek juga konsistensi visual, teks, aksesibilitas, dan kondisi seperti gagal simpan atau batal hapus.
- Catat temuan sebagai **Observasi → Dampak → Saran perbaikan**. Sebutkan layar, komponen, atau kondisi terkait. Misalnya, ganti tombol **Ya** di dialog hapus dengan **Hapus produk** agar tindakannya jelas.
- Dahulukan hambatan yang menghalangi tugas, menyamarkan konsekuensi, atau mencegah pemulihan. Perbaiki dalam cakupan dan cek ulang. Tanya lewat chat dengan opsi dan rekomendasi bila perlu keputusan produk.
- Jika asumsi penting belum diuji, usulkan tugas realistis di wireframe atau prototipe. Misalnya, amati apakah pengguna yang memperbarui stok menemukan aksi edit, memahami konfirmasi, dan mengenali hasil simpan.

## Hasil rancangan

Gunakan Bahasa Indonesia untuk PRD, spesifikasi, dan pertanyaan di chat. Gunakan Bahasa Indonesia untuk teks antarmuka jika bahasa produk belum ditentukan. Jika produk punya bahasa tersendiri, tulis contoh teks antarmuka dalam bahasa produk.

Sertakan ringkasan tugas, layout dalam urutan baca, komponen dan varian, keputusan visual dan token, kondisi dan transisi dengan usulan teks, aturan responsif dan aksesibilitas, serta asumsi atau pertanyaan terbuka.

Untuk kode, jelaskan bagian halaman, varian shadcn/ui, pemicu, dan hasil yang perlu diterapkan. Untuk Figma, jelaskan frame, varian kondisi, komponen serta token pustaka, dan interaksi prototipe. Gunakan nama kondisi, teks, dan keputusan yang konsisten jika kedua tujuan diminta.

### Alur kerja Figma

- Jika pengguna memberikan desain Figma, periksa frame, instans, properti, dan varian terkait lewat integrasi yang tersedia. Tentukan kondisi dan transisi yang masih dibutuhkan. Jika hanya ada tangkapan layar atau deskripsi, nyatakan asumsi.
- Petakan kondisi ke frame atau varian yang diberi nama. Tentukan interaksi penting, misalnya **Hapus** membuka konfirmasi, pembatalan kembali ke daftar, dan persetujuan menampilkan proses serta hasil.
- Untuk membuat atau memperbarui tampilan langsung di Figma, gunakan `figma:figma-generate-design` bersama `figma:figma-use`. Pakai spesifikasi UX sebagai brief dan gunakan komponen, varian, serta token pustaka jika tersedia. Ikuti `figma:figma-use` sebelum setiap panggilan `use_figma`, termasuk untuk pemeriksaan terprogram. Gunakan `figma:figma-create-new-file` jika diminta membuat file baru. Untuk rancangan siap Figma, serahkan spesifikasinya.

## Referensi

Gunakan [panduan komponen](references/components.md) untuk mencari pilihan. Cek perilaku dan varian di [dokumentasi resmi shadcn/ui](https://ui.shadcn.com/docs/components).
