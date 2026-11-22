# Panduan komponen shadcn/ui

Gunakan panduan ini untuk memilih keluarga komponen yang sesuai dengan tugas pengguna. Utamakan komponen yang diberikan pengguna atau tersedia di proyek. Jika daftar belum ada, cek pilihan dan perilakunya di [dokumentasi resmi](https://ui.shadcn.com/docs/components) dan tandai pilihan sebagai usulan. Catat kebutuhan yang belum tercakup dalam spesifikasi UX.

## Navigasi dan orientasi

| Kebutuhan pengguna | Komponen yang bisa dipilih |
| --- | --- |
| Berpindah antarbagian | Navigation Menu, Menubar, Sidebar |
| Menunjukkan posisi saat ini | Breadcrumb, Tabs |
| Menelusuri hasil yang panjang | Pagination, Scroll Area |
| Membuka aksi sesuai konteks | Dropdown Menu, Context Menu |

## Formulir dan input

| Kebutuhan pengguna | Komponen yang bisa dipilih |
| --- | --- |
| Mengisi teks pendek atau panjang | Input, Textarea, Input Group |
| Memilih satu atau beberapa nilai | Native Select, Select, Combobox, Checkbox, Radio Group, Toggle Group |
| Mengatur pilihan ya atau tidak | Switch |
| Menentukan rentang angka | Slider |
| Mengisi tanggal | Calendar, Date Picker |
| Mengisi kode sekali pakai | Input OTP |
| Mengelompokkan, melabeli, dan menjelaskan kolom | Field, Label |
| Mengirim isian terkait | Pola formulir dengan Button dan pesan validasi yang jelas |

## Aksi dan pilihan

| Kebutuhan pengguna | Komponen yang bisa dipilih |
| --- | --- |
| Menjalankan aksi utama atau tambahan | Button, Button Group |
| Mengaktifkan atau menonaktifkan satu opsi | Toggle |
| Memilih dari hasil pencarian perintah | Command |
| Mengonfirmasi aksi yang berdampak | Alert Dialog |

## Informasi dan status

| Kebutuhan pengguna | Komponen yang bisa dipilih |
| --- | --- |
| Menampilkan pesan ringkas atau status | Alert, Message, Badge |
| Menampilkan konfirmasi atau pembaruan sementara | Toast |
| Menunjukkan progres proses | Progress |
| Menunjukkan aktivitas atau bentuk konten yang sedang dimuat | Spinner, Skeleton |
| Menjelaskan kontrol saat dibutuhkan | Tooltip, Hover Card |
| Menampilkan identitas pengguna | Avatar |
| Memberi petunjuk saat konten kosong | Empty |
| Menampilkan atau memformat konten | Card, Item, Typography, Separator, Aspect Ratio |
| Menampilkan pintasan keyboard | Kbd |

## Overlay dan informasi bertahap

| Kebutuhan pengguna | Komponen yang bisa dipilih |
| --- | --- |
| Menampilkan keputusan atau tugas singkat | Dialog |
| Menampilkan panel yang sesuai untuk mobile | Drawer, Sheet |
| Menampilkan informasi tambahan dekat pemicu | Popover, Hover Card |
| Membuka detail tambahan di tempat | Accordion, Collapsible |

## Data dan konten

| Kebutuhan pengguna | Komponen yang bisa dipilih |
| --- | --- |
| Membandingkan data terstruktur | Table, Data Table |
| Menelusuri rangkaian item visual | Carousel |
| Menampilkan grafik | Chart |
| Menampilkan pratinjau media dengan rasio tetap | Aspect Ratio |
| Melampirkan atau menampilkan file | Attachment |

## Komponen khusus dan pendukung

Cek dokumentasi tiap komponen untuk memahami pola interaksinya sebelum memilih.

| Komponen | Peran dalam UX |
| --- | --- |
| Bubble | Menampilkan pesan singkat atau bagian percakapan |
| Code Block | Menampilkan kode untuk dibaca atau disalin |
| Direction | Mengatur atau menunjukkan arah teks dan layout |
| Marker | Menandai bagian tertentu dalam konten |
| Message Scroller | Menampilkan rangkaian pesan yang dapat digulir |
| Questionnaire | Memandu pengguna melalui serangkaian pertanyaan |
| Resizable | Memungkinkan pengguna mengatur lebar atau tinggi panel bersebelahan |
| Trace | Menampilkan jejak atau rangkaian terstruktur untuk diperiksa |

## Pertanyaan tinjauan

Untuk tiap komponen, periksa:

1. Tugas apa yang didukung dan mengapa pola interaksinya sesuai?
2. Informasi dan aksi apa yang harus terlihat sebelum pengguna mengambil keputusan?
3. Kondisi apa yang relevan, seperti nonaktif, memuat, terpilih, kosong, gagal, dan berhasil?
4. Bagaimana perilakunya dengan keyboard, sentuhan, layar sempit, dan teknologi bantu?
5. Bagaimana pengguna menutup, membatalkan, atau memulihkan interaksi?

Cek indeks resmi sebelum menambahkan atau menghapus keluarga komponen dari panduan ini.
