# 😂 Meme Generator Dinamis

[🇮🇩 Bahasa Indonesia](#-bahasa-indonesia) · [🇬🇧 English](#-english)

---

## 🇮🇩 Bahasa Indonesia

Pembuat meme sederhana yang berjalan **sepenuhnya di browser**. Cukup satu file HTML, tanpa build, tanpa server, tanpa instalasi.

> 🔒 **Privasi:** gambar yang kamu pilih hanya di-render di perangkatmu (client side, bukan server side), jadi tidak ada yang disimpan atau diunggah ke mana pun.

**Live demo:** [https://bikin-meme.vercel.app/](https://bikin-meme.vercel.app/)

### ✨ Fitur

- **Ukuran otomatis:** canvas mengikuti rasio foto asli (portrait maupun landscape), tanpa area kosong.
- **Banyak teks:** sampai 6 teks, masing-masing dengan ukuran huruf, posisi vertikal dan posisi horizontal sendiri.
- **Pilihan font:** Bawaan (Noto Sans), **Impact** (klasik) dan **Anton** (alternatif Impact yang gratis).
- **Warna & stroke:** warna teks, warna stroke dan ketebalan stroke bisa diatur.
- **Bentuk gambar:** Kotak (Square) atau Rounded (PNG dengan sudut transparan).
- **Dua bahasa:** Indonesia dan Inggris, otomatis mengikuti bahasa browser dan tersimpan di `localStorage`.
- **Responsif:** preview menempel di atas (HP) atau di kiri (PC dan HP landscape), kontrol dibagi dalam tab Teks, Gaya dan Gambar.
- **Download PNG:** hasil download sama persis dengan preview.

### 🚀 Cara pakai

1. Buka `index.html` di browser, atau jalankan lewat Live Server di VS Code.
2. Klik **Pilih File** dan pilih foto.
3. Isi teks, atur ukuran dan posisinya, lalu pilih font, warna dan stroke di tab **Gaya**.
4. Klik **Download PNG**.

> Butuh koneksi internet saat pertama dibuka, karena Tailwind CSS dan font Anton dimuat dari CDN. Foto kamu tetap tidak pernah dikirim ke mana pun.

### 🔤 Catatan font

- **Impact** adalah font bawaan sistem, ada di Windows dan Mac tetapi tidak di banyak HP Android. Jika tidak tersedia, otomatis dipakai **Anton**.
- **Anton** hanya punya satu ketebalan, jadi tidak diberi bold palsu.
- Karakter yang tidak ada di Anton atau Impact (mis. Hangul) otomatis memakai font bawaan.

### ⚙️ Kustomisasi

Semua pengaturan ada di bagian `<script>` pada `index.html`:

| Konstanta | Fungsi | Default |
| --- | --- | --- |
| `MAX_LAYERS` | Jumlah maksimal teks | `6` |
| `MAX_SIDE` | Sisi terpanjang canvas (batas aman) | `4096` |
| `REF_WIDTH` | Lebar acuan untuk skala ukuran huruf | `600` |
| `FONTS` | Daftar font dan ketebalannya | Bawaan, Impact, Anton |
| `link.download` | Nama file hasil download | `meme-hachiware.png` |

Untuk menambah bahasa, tambahkan satu objek baru di `I18N` dan satu tombol di header.

### 🌐 Deploy ke GitHub Pages

1. Pastikan file bernama `index.html` di root repo.
2. Buka **Settings → Pages**.
3. Pilih **Deploy from a branch**, branch `main`, folder `/ (root)`, lalu **Save**.
4. Tunggu beberapa menit, situsmu akan aktif di `https://<username>.github.io/<nama-repo>/`.

### 🧰 Teknologi

- HTML, CSS dan JavaScript murni (tanpa framework)
- [Tailwind CSS](https://tailwindcss.com) (Play CDN)
- Canvas API untuk render dan export PNG
- [Anton](https://fonts.google.com/specimen/Anton) dari Google Fonts

### 📄 Lisensi

Tambahkan file `LICENSE` sesuai pilihanmu (mis. MIT).

---

## 🇬🇧 English

A simple meme maker that runs **entirely in your browser**. One HTML file: no build step, no server, no install.

> 🔒 **Privacy:** the image you pick is only rendered on your device (client side, not server side), so nothing is stored or uploaded anywhere.

**Live demo:** [https://bikin-meme.vercel.app/](https://bikin-meme.vercel.app/)

### ✨ Features

- **Automatic sizing:** the canvas follows the original photo's aspect ratio (portrait or landscape), with no empty space.
- **Multiple texts:** up to 6 texts, each with its own font size, vertical position and horizontal position.
- **Font choices:** Default (Noto Sans), **Impact** (classic) and **Anton** (a free Impact-like alternative).
- **Color & stroke:** adjustable text color, stroke color and stroke width.
- **Image shape:** Square or Rounded (PNG with transparent corners).
- **Bilingual:** Indonesian and English, auto-detected from the browser language and remembered in `localStorage`.
- **Responsive:** the preview sticks to the top (phones) or the left (desktop and landscape phones), and controls are split into Text, Style and Image tabs.
- **PNG download:** the downloaded file matches the preview exactly.

### 🚀 Usage

1. Open `index.html` in a browser, or serve it with VS Code Live Server.
2. Click **Choose File** and pick a photo.
3. Enter your text, adjust size and position, then pick font, color and stroke in the **Style** tab.
4. Click **Download PNG**.

> An internet connection is needed on first load, because Tailwind CSS and the Anton font come from CDNs. Your photo is still never sent anywhere.

### 🔤 Font notes

- **Impact** is a system font: available on Windows and Mac, but not on many Android phones. If it's missing, **Anton** is used automatically.
- **Anton** has a single weight, so no fake bold is applied.
- Characters missing from Anton or Impact (e.g. Hangul) fall back to the default font.

### ⚙️ Customization

Everything lives in the `<script>` section of `index.html`:

| Constant | Purpose | Default |
| --- | --- | --- |
| `MAX_LAYERS` | Maximum number of texts | `6` |
| `MAX_SIDE` | Longest canvas side (safety limit) | `4096` |
| `REF_WIDTH` | Reference width for font size scaling | `600` |
| `FONTS` | Font list and weights | Default, Impact, Anton |
| `link.download` | Downloaded file name | `meme-hachiware.png` |

To add a language, add a new object to `I18N` and a button in the header.

### 🌐 Deploy to GitHub Pages

1. Make sure the file is named `index.html` at the repo root.
2. Go to **Settings → Pages**.
3. Choose **Deploy from a branch**, branch `main`, folder `/ (root)`, then **Save**.
4. Wait a few minutes; your site will be live at `https://<username>.github.io/<repo-name>/`.

### 🧰 Tech stack

- Plain HTML, CSS and JavaScript (no framework)
- [Tailwind CSS](https://tailwindcss.com) (Play CDN)
- Canvas API for rendering and PNG export
- [Anton](https://fonts.google.com/specimen/Anton) from Google Fonts

### 📄 License

Add a `LICENSE` file of your choice (e.g. MIT).
