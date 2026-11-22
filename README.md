# Skill UX 70s

Skill untuk merancang alur, layout shadcn/ui, kondisi layar, dan microcopy sebelum halaman dibuat lewat kode atau di Figma.

## Instal lewat chat AI agent

Salin prompt ini ke chat AI agent di proyek tujuan.

```text
Tolong instal Skill UX 70s di proyek ini dan targetkan instalasinya ke AI agent yang sedang saya pakai. Gunakan perintah berikut, lalu cek apakah skill-ux-70s sudah terpasang.

npx skills add ihsan70s/skill-ux-70s --skill skill-ux-70s
```

Repo ini privat. Akun GitHub yang dipakai saat instalasi perlu punya akses ke repo.

## Instal dari folder lokal lewat npx

Jalankan dari terminal di proyek tujuan. Instalasi ini memerlukan Node.js 22.20 atau lebih baru.

```powershell
npx skills add '../skill-ux-70s' --skill skill-ux-70s --agent codex --copy
```

Contoh ini mengasumsikan folder `skill-ux-70s` berada di sebelah folder proyek tujuan. Sesuaikan path dengan lokasi folder skill di komputermu. Tambahkan `--global` untuk memasang skill bagi semua proyek. Setelah terpasang, panggil `$skill-ux-70s` di chat Codex.

[Dokumentasi CLI skills](https://github.com/vercel-labs/skills#install-a-skill)

## Instal manual di Codex

1. Pilih lokasi pemasangan.
   - **Satu proyek (disarankan untuk tim).** Buat folder `.agents/skills/skill-ux-70s` di root proyek tujuan.
   - **Semua proyek di akun Windows kamu.** Buat folder `%USERPROFILE%\.agents\skills\skill-ux-70s`. Masukkan path itu di bilah alamat File Explorer untuk membukanya setelah dibuat.
2. Salin `SKILL.md`, folder `agents`, dan folder `references` ke lokasi yang dipilih. Pastikan susunannya seperti ini.

   ```text
   skill-ux-70s/
   ├── SKILL.md
   ├── agents/
   │   └── openai.yaml
   └── references/
       └── components.md
   ```

3. Buka proyek di Codex dan panggil `$skill-ux-70s` di chat. Kalau skill belum muncul, mulai ulang Codex.

## Contoh pemakaian

```text
$skill-ux-70s Rancang halaman daftar produk dengan komponen shadcn/ui.
Sertakan alur tambah, edit, dan hapus produk, termasuk dialog konfirmasi dan kondisi gagal.
```

Untuk membuat atau mengedit desain langsung di file Figma, pastikan integrasi Figma tersedia di sesi Codex. Rancangan UX siap Figma bisa diminta dari skill ini lewat chat.

[Dokumentasi resmi pemasangan skill lokal di Codex](https://learn.chatgpt.com/docs/build-skills#where-codex-loads-local-skills)
