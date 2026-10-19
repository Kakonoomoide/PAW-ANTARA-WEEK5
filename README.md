# Week 5 Revision — Etalase & Caption

Dua halaman web statis (HTML + CSS + JS native, tanpa library) yang terhubung lewat nav bar sticky.

## Halaman

### Etalase (`index.html`)
Katalog produk yang datanya diambil dari [dummyjson.com/products](https://dummyjson.com/products).
- Cari produk berdasarkan nama
- Filter berdasarkan kategori
- Badge "Stok Menipis" untuk produk dengan stok di bawah 10

### Caption (`form.html`)
Generator caption produk untuk media sosial.
1. Isi **nama produk** dan **harga**
2. Pilih template: **Promo**, **Santai**, atau **Formal**
3. Klik **Buat Caption**, lalu caption lengkap dengan emoji dan hashtag muncul di bawah

Harga otomatis diformat ke Rupiah, nama produk otomatis dijadikan hashtag (`kopi susu aren` → `#KopiSusuAren`).

**Validasi** (pesan error muncul langsung di bawah input saat mengetik):

| Field | Aturan |
|---|---|
| Nama Produk | wajib, 3–60 karakter, harus mengandung huruf |
| Harga | wajib, angka bulat, Rp 1.000 – Rp 100.000.000 |

## Struktur File

| File | Isi |
|---|---|
| `index.html` / `index.js` | Halaman Etalase dan logika fetch, cari, filter |
| `index.css` | Style utama yang dipakai **kedua** halaman (warna, font, nav, header, footer) |
| `form.html` / `form.js` | Halaman Caption, template caption, dan validasi |
| `form.css` | Style khusus form (dimuat setelah `index.css`) |
| `fetch.js` | Script uji coba fetch API |
| `test.js` | Script latihan |

## Cara Menjalankan

Buka `index.html` di browser. Tidak perlu install apa pun, tapi halaman Etalase butuh koneksi internet untuk mengambil data produk.

## Kustomisasi

- **Tambah template caption:** tambahkan entri baru di objek `templates` di `form.js`, lalu tambahkan `<option>` dengan `value` yang sama di `form.html`.
- **Ubah batas validasi:** edit objek `rules` di `form.js`.
- **Tambah halaman baru:** tambahkan link di `<nav>` pada setiap file HTML, dan beri `aria-current="page"` pada link halaman yang sedang aktif.
