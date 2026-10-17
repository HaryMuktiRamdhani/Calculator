<div align="center">

# Tugas Calculator

Kalkulator web sederhana yang dibangun dengan HTML, CSS, dan JavaScript murni.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Dependensi](https://img.shields.io/badge/dependensi-nol-22C55E?style=flat)

<img src="docs/simulasi.svg" alt="Simulasi kalkulator beranimasi: perkalian, pembagian, backspace, dan pesan error" width="360">

</div>

---

## Ringkasan

Tugas Calculator adalah kalkulator berbasis web yang dibuat sebagai tugas latihan pemrograman web. Seluruh logikanya ditulis dengan JavaScript tanpa framework maupun library, dan tampilannya dengan CSS biasa. Tidak ada proses build: cukup buka `index.html` di browser.

Kalkulator dapat dioperasikan dengan klik pada tombol maupun lewat keyboard. Jika ekspresi yang dimasukkan tidak valid, layar menampilkan `Error`.

Hal yang menjadi fokus pengembangan:

- **Sederhana** — tiga berkas, tanpa konfigurasi
- **Tanpa dependensi** — tidak ada package yang perlu diinstal
- **Dua cara input** — mouse dan keyboard
- **Tahan salah input** — ekspresi tidak valid ditangani, tidak merusak tampilan

## Tampilan

<div align="center">

<img src="docs/screenshot.png" alt="Tampilan kalkulator yang menampilkan hasil 12 x 4 + 8 = 56" width="380">

<sub>Tampilan kalkulator setelah menghitung <code>12 x 4 + 8</code></sub>

</div>

Animasi di bagian atas halaman ini adalah simulasi otomatis yang berulang: `12 x 4 + 8`, `9 ÷ 4`, `500 ⌫ + 25`, lalu ekspresi tidak valid yang menampilkan `Error`.

## Fitur

**Operasi**

- Penjumlahan, pengurangan, perkalian, dan pembagian
- Operator modulo (`%`) untuk sisa bagi
- Bilangan desimal dengan tombol titik
- Tombol `00` untuk input angka lebih cepat

**Input dan kontrol**

- Tombol `C` untuk mengosongkan layar
- Tombol `⌫` untuk menghapus satu karakter terakhir
- Dukungan keyboard untuk semua operasi utama
- Pesan `Error` untuk ekspresi yang tidak valid

**Tampilan**

- Layout terpusat dengan Flexbox
- Layar hasil rata kanan
- Tombol hapus (`C` dan `⌫`) berwarna oranye sebagai pembeda

## Stack

| Bagian | Teknologi | Keterangan |
|---|---|---|
| Struktur | HTML5 | Layar dan tombol berbasis `<input>` dalam satu form |
| Tampilan | CSS3 | Flexbox untuk pemusatan dan tata letak layar |
| Logika | JavaScript | Manipulasi DOM dan penanganan event |

## Kontrol Keyboard

| Tombol | Aksi |
|---|---|
| `0` - `9` | Memasukkan angka |
| `+` `-` `*` `/` | Tambah, kurang, kali, bagi |
| `x` | Kali (ditampilkan sebagai `x`) |
| `.` | Titik desimal |
| `%` | Modulo |
| `Enter` | Menghitung hasil |
| `Backspace` | Menghapus satu karakter terakhir |
| `C` | Mengosongkan layar |

## Arsitektur

```
.
├── docs/
│   ├── screenshot.png
│   └── simulasi.svg
└── tugas membuat kalkulator/
    ├── index.html     Struktur dan tombol kalkulator
    ├── style.css      Tampilan
    └── index.js       Logika dan input keyboard
```

**Alur kerja.** Setiap tombol memanggil fungsi di `index.js` lewat atribut `onclick`. Angka dan operator ditambahkan ke layar oleh `Solve(val)`, sedangkan `Result()` mengevaluasi ekspresi di layar dan menampilkan hasilnya. Jika evaluasi gagal, layar menampilkan `Error`. Input keyboard ditangani oleh satu event listener `keydown` yang meneruskan tombol ke fungsi yang sama.

| Fungsi | Peran |
|---|---|
| `Solve(val)` | Menambahkan angka atau operator ke layar |
| `Result()` | Mengevaluasi ekspresi di layar, menampilkan hasil atau `Error` |
| `Clear()` | Mengosongkan layar |
| `Back()` | Menghapus satu karakter terakhir |
| Event `keydown` | Menghubungkan input keyboard ke fungsi di atas |

## Catatan Teknis

- Ekspresi dievaluasi dengan `eval()`. Ini praktis untuk proyek latihan dan penggunaan lokal, tetapi untuk aplikasi produksi sebaiknya diganti dengan parser ekspresi.
- Operator `%` bekerja sebagai **modulo** (sisa bagi) seperti di JavaScript, bukan persentase. Contoh: `10 % 3` menghasilkan `1`.

## Development

Prasyarat: browser modern. Tidak ada dependensi yang perlu diinstal.

```bash
git clone https://github.com/HaryMuktiRamdhani/Tugas-Calculator.git
cd Tugas-Calculator/"tugas membuat kalkulator"
```

| Cara | Langkah |
|---|---|
| Langsung | Buka `index.html` di browser |
| Server lokal | Jalankan `python -m http.server 8000`, lalu buka `http://localhost:8000` |

## Author

Hary Mukti Ramdhani — [@HaryMuktiRamdhani](https://github.com/HaryMuktiRamdhani)
