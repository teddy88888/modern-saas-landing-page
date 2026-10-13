# Landing Page dengan Tailwind CSS

> Tailwind adalah salah satu framework CSS yang paling banyak dipakai di industri saat ini. Belajar Tailwind sekarang akan sangat membantumu di project-project nyata ke depannya. Luangkan waktu untuk memahami _kenapa_ setiap utility class itu bekerja, bukan sekadar _apa_ fungsinya.

## Gambaran Umum

|                      |                                                                                                                        |
| -------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| **Week**             | 3                                                                                                                      |
| **Branch**           | `feat/tailwind`                                                                                                        |
| **Tech Stack**       | HTML, Tailwind CSS                                                                                                     |
| **Referensi Desain** | [Buka Figma](https://www.figma.com/design/V8GNQPn1cu1NknDYWKrE49/Challenge-2?node-id=8411-143671&t=Fi9CakO96MRdz4g1-1) |

---

## Tujuan

Bangun landing page menggunakan **Tailwind CSS**. Tidak boleh ada CSS tradisional sama sekali.

belajar cara menerjemahkan desain Figma menjadi halaman web yang responsif, hanya dengan menggunakan utility class dari Tailwind.

---

## Struktur Folder

```
wph-assignment-3/
├── src/
│   ├── input.css        # File CSS utama Tailwind
│   ├── output.css       # Dibuat otomatis oleh Tailwind CLI
│   └── index.html       # File HTML utama kamu
├── assets/
│   ├── images/          # Simpan semua file gambar
│   └── icons/           # Simpan semua file icon (SVG, PNG)
├── package.json         # Konfigurasi Node dan dependency
├── README.md            # File
└── .gitignore           # Daftar file yang tidak ikut di-commit ke Git
```

> **Penting:** File `src/output.css` dibuat secara otomatis oleh Tailwind. Jangan pernah mengeditnya secara manual dan jangan di-commit ke Git.

---

## Ketentuan Assignment

### Wajib Dipenuhi

- [ ] Semua styling menggunakan **Tailwind CSS** saja, tidak boleh ada custom CSS kecuali `@apply`
- [ ] Halaman harus **responsif**, tampil baik di mobile maupun desktop
- [ ] Gunakan utility class Tailwind untuk semua keperluan styling: spacing, typography, warna, dan layout
- [ ] Tidak boleh ada CSS tradisional seperti `.nama-class { color: red }`

### Komponen Minimum

Halaman harus memiliki ketiga bagian ini:

| Komponen         | Keterangan                                                   |
| ---------------- | ------------------------------------------------------------ |
| **Navbar**       | Navigasi halaman, responsif di mobile                        |
| **Hero Section** | Bagian utama berisi headline, teks pendukung, dan tombol CTA |
| **Footer**       | Berisi link, copyright, atau informasi kontak                |

tambahkan section lain dari desain Figma kamu. Ketiga komponen di atas adalah minimal.

---

## Langkah-Langkah Pengerjaan

### Langkah 1 - Branch Baru

```bash
git checkout -b feat/tailwind
```

branch `feat/tailwind`. Jangan pernah commit langsung ke `main`.

### Langkah 2 - Install Dependencies

install [Node.js](https://nodejs.org) di komputer, lalu jalankan:

```bash
npm install
```

Perintah ini akan menginstall `tailwindcss` dan `@tailwindcss/cli` sesuai yang sudah tercantum di `package.json`.

### Langkah 3 - Jalankan Tailwind CLI

```bash
npm run dev
```

Perintah ini akan memantau perubahan di file HTML dan secara otomatis memperbarui file `src/output.css` setiap kali kamu menyimpan file.

> Biarkan terminal ini tetap berjalan selama kamu bekerja. Jangan ditutup.

Berikut penjelasan dari perintah yang dijalankan di balik layar:

```
npx @tailwindcss/cli -i ./src/input.css -o ./src/output.css --watch
```

| Bagian                | Artinya                                             |
| --------------------- | --------------------------------------------------- |
| `-i ./src/input.css`  | File CSS input yang berisi `@import "tailwindcss"`  |
| `-o ./src/output.css` | File CSS output yang akan dimuat oleh HTML          |
| `--watch`             | Otomatis rebuild setiap kali ada file yang disimpan |

### Langkah 4 - Pelajari Desain Figma Sebelum Mulai Coding

Buka file [Figma](https://www.figma.com/design/V8GNQPn1cu1NknDYWKrE49/Challenge-2?node-id=8411-143671&t=Fi9CakO96MRdz4g1-1) dan perhatikan hal-hal berikut sebelum menulis satu baris pun kode:

- Warna yang digunakan (kode hex)
- Ukuran dan ketebalan font
- Jarak antar elemen (padding dan margin)
- Struktur layout (apakah menggunakan flex atau grid?)
- Bagian mana yang berubah tampilan di mobile vs desktop

**Rencanakan dulu, baru coding.**

### Langkah 5 - Bangun Halaman Section per Section

Jangan langsung mengerjakan semua sekaligus. Kerjakan satu section dulu sampai selesai:

1. Tulis dulu **struktur HTML**-nya menggunakan tag yang semantik, tanpa styling apapun
2. Tambahkan **Tailwind class** untuk mencocokkan tampilan dengan desain Figma
3. Cek **responsivitas** di browser menggunakan DevTools (mode mobile)
4. Lanjut ke section berikutnya

### Langkah 6 - Cek Responsivitas

Sebelum submit, pastikan halaman kamu terlihat baik di semua ukuran layar berikut:

| Breakpoint | Lebar Layar       | Prefix Tailwind         |
| ---------- | ----------------- | ----------------------- |
| Mobile     | kurang dari 640px | (default, tanpa prefix) |
| Tablet     | 768px ke atas     | `md:`                   |
| Desktop    | 1024px ke atas    | `lg:`                   |

Cara cek: buka Chrome, klik kanan di halaman, pilih **Inspect**, lalu aktifkan **Toggle Device Toolbar** (ikon handphone di pojok kiri atas panel DevTools).

### Langkah 7 - Push ke GitHub

Setelah semua selesai, push pekerjaanmu ke GitHub:

```bash
git add .
git commit -m "feat: build landing page with tailwind css"
git push origin feat/tailwind
```

Setelah itu, buka repositorimu di GitHub dan buat **Pull Request** dari branch `feat/tailwind` ke `main`.

---

## Checklist Sebelum Submit

Pastikan semua poin ini sudah terpenuhi sebelum kamu mengumpulkan:

- [ ] Semua styling menggunakan Tailwind utility class
- [ ] Tidak ada custom CSS (kecuali `@apply` jika digunakan)
- [ ] Navbar sudah ada dan berfungsi
- [ ] Hero section sudah ada
- [ ] Footer sudah ada
- [ ] Halaman responsif di mobile dan desktop
- [ ] Tailwind breakpoints (`sm:`, `md:`, `lg:`) digunakan sesuai kebutuhan
- [ ] Kode rapi, indentasi benar, tidak ada kode yang tidak terpakai
- [ ] Project sudah di-push ke GitHub di branch `feat/tailwind`
- [ ] Pull Request sudah dibuat di GitHub

---

## Tips dan Kesalahan Umum

**Yang harus dilakukan:**

- Selalu gunakan prefix responsif Tailwind: `sm:`, `md:`, `lg:`
- Gunakan utility `flex` dan `grid` untuk mengatur layout
- Buka [dokumentasi Tailwind](https://tailwindcss.com/docs) sambil bekerja, jadikan referensi utama
- Usahakan spacing dan ukuran font semirip mungkin dengan desain Figma

**Yang harus kamu hindari:**

- Menulis CSS di dalam tag `<style>` (kecuali untuk `@apply`)
- Menggunakan atribut `style=""` langsung di HTML
- Tidak mengecek tampilan mobile sebelum submit
- Menyalin class Tailwind tanpa memahami apa fungsi masing-masing class

---

## Referensi

| Sumber                          | Link                                                                                                     |
| ------------------------------- | -------------------------------------------------------------------------------------------------------- |
| Dokumentasi Tailwind CSS        | https://tailwindcss.com/docs                                                                             |
| Tailwind Cheat Sheet            | https://nerdcave.com/tailwind-cheat-sheet                                                                |
| Referensi Desain Figma          | https://www.figma.com/design/V8GNQPn1cu1NknDYWKrE49/Challenge-2?node-id=8411-143671&t=Fi9CakO96MRdz4g1-1 |
| Chrome DevTools (Cek Responsif) | https://developer.chrome.com/docs/devtools/device-mode                                                   |

---

## Kriteria Penilaian

| Kriteria                                                  | Bobot |
| --------------------------------------------------------- | ----- |
| Penggunaan Tailwind CSS yang benar (tidak ada custom CSS) | 30%   |
| Desain responsif (mobile dan desktop)                     | 25%   |
| Kemiripan visual dengan desain Figma                      | 25%   |
| Kebersihan dan kerapian kode                              | 10%   |
| Git workflow yang benar dan Pull Request                  | 10%   |
