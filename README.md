<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,100:2563eb&height=200&section=header&text=Tugas%20Calculator&fontColor=ffffff&fontSize=48&fontAlignY=38&desc=Kalkulator%20web%20sederhana%20dengan%20HTML%2C%20CSS%2C%20dan%20JavaScript&descAlignY=60&descSize=17" alt="Tugas Calculator" width="100%">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1200&color=38BDF8&center=true&vCenter=true&width=640&lines=Kalkulator+berbasis+web;Bisa+diklik+atau+diketik+lewat+keyboard;Tanpa+framework%2C+tanpa+dependensi)](#demo)

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Dependensi](https://img.shields.io/badge/Dependensi-Tidak%20ada-22C55E?style=for-the-badge)

<a href="#demo"><img src="https://api.iconify.design/lucide/circle-play.svg?color=%2338bdf8" width="16" alt=""></a> <a href="#demo">Demo</a> &nbsp;&middot;&nbsp;
<a href="#fitur"><img src="https://api.iconify.design/lucide/sparkles.svg?color=%2338bdf8" width="16" alt=""></a> <a href="#fitur">Fitur</a> &nbsp;&middot;&nbsp;
<a href="#kontrol-keyboard"><img src="https://api.iconify.design/lucide/keyboard.svg?color=%2338bdf8" width="16" alt=""></a> <a href="#kontrol-keyboard">Keyboard</a> &nbsp;&middot;&nbsp;
<a href="#cara-kerja"><img src="https://api.iconify.design/lucide/workflow.svg?color=%2338bdf8" width="16" alt=""></a> <a href="#cara-kerja">Cara Kerja</a> &nbsp;&middot;&nbsp;
<a href="#menjalankan"><img src="https://api.iconify.design/lucide/terminal.svg?color=%2338bdf8" width="16" alt=""></a> <a href="#menjalankan">Menjalankan</a>

</div>

---

## Ringkasan

Tugas Calculator adalah kalkulator berbasis web yang dibangun murni dengan HTML, CSS, dan JavaScript. Tidak ada framework, library, maupun proses build: cukup buka `index.html` di browser dan kalkulator langsung bisa dipakai.

Kalkulator dapat dioperasikan dengan klik pada tombol maupun lewat keyboard, dan menampilkan pesan `Error` ketika ekspresi yang dimasukkan tidak valid.

---

## Demo

<div align="center">

<img src="docs/demo.gif" alt="Demo kalkulator: menghitung 12 x 4 + 8 dengan hasil 56" width="320">

<br>

<sub>Contoh perhitungan <code>12 x 4 + 8</code> dengan hasil <code>56</code></sub>

</div>

---

## Fitur

| Fitur | Keterangan |
|---|---|
| <img src="https://api.iconify.design/lucide/calculator.svg?color=%232563eb" width="20" align="center" alt=""> &nbsp;**Operasi dasar** | Penjumlahan, pengurangan, perkalian, dan pembagian |
| <img src="https://api.iconify.design/lucide/percent.svg?color=%232563eb" width="20" align="center" alt=""> &nbsp;**Modulo** | Operator `%` untuk sisa bagi |
| <img src="https://api.iconify.design/lucide/hash.svg?color=%232563eb" width="20" align="center" alt=""> &nbsp;**Bilangan desimal dan `00`** | Tombol titik dan tombol `00` untuk input angka lebih cepat |
| <img src="https://api.iconify.design/lucide/eraser.svg?color=%232563eb" width="20" align="center" alt=""> &nbsp;**Hapus cepat** | `C` mengosongkan layar, `⌫` menghapus satu karakter terakhir |
| <img src="https://api.iconify.design/lucide/keyboard.svg?color=%232563eb" width="20" align="center" alt=""> &nbsp;**Dukungan keyboard** | Semua operasi utama bisa dilakukan tanpa mouse |
| <img src="https://api.iconify.design/lucide/triangle-alert.svg?color=%232563eb" width="20" align="center" alt=""> &nbsp;**Penanganan error** | Ekspresi tidak valid menampilkan `Error`, bukan merusak tampilan |
| <img src="https://api.iconify.design/lucide/package.svg?color=%232563eb" width="20" align="center" alt=""> &nbsp;**Tanpa dependensi** | Tiga berkas saja, langsung jalan di browser mana pun |

---

## Kontrol Keyboard

| Tombol | Aksi |
|---|---|
| `0` - `9` | Memasukkan angka |
| `+` `-` `*` `/` | Operator tambah, kurang, kali, bagi |
| `x` | Operator kali (ditampilkan sebagai `x`) |
| `.` | Titik desimal |
| `%` | Modulo |
| `Enter` | Menghitung hasil |
| `Backspace` | Menghapus satu karakter terakhir |
| `C` | Mengosongkan layar |

---

## Cara Kerja

```mermaid
flowchart LR
    A[Klik tombol<br/>atau tekan keyboard] --> B["Solve(val)<br/>tambah ke layar"]
    B --> C["Result()<br/>evaluasi ekspresi"]
    C --> D{Valid?}
    D -- Ya --> E[Tampilkan hasil]
    D -- Tidak --> F[Tampilkan Error]
```

| Fungsi | Peran |
|---|---|
| `Solve(val)` | Menambahkan angka atau operator ke layar |
| `Result()` | Mengevaluasi ekspresi di layar dan menampilkan hasilnya, atau `Error` jika gagal |
| `Clear()` | Mengosongkan layar |
| `Back()` | Menghapus satu karakter terakhir |
| Event `keydown` | Menghubungkan input keyboard ke fungsi-fungsi di atas |

---

## Teknologi

| Bagian | Teknologi | Keterangan |
|---|---|---|
| Struktur | HTML5 | Layar dan tombol kalkulator berbasis `<input>` dalam satu form |
| Tampilan | CSS3 | Flexbox untuk pemusatan dan tata letak layar |
| Logika | JavaScript | Manipulasi DOM dan penanganan event |

---

## Struktur

```
.
├── docs/
│   ├── demo.gif
│   └── preview.png
└── tugas membuat kalkulator/
    ├── index.html     Struktur dan tombol kalkulator
    ├── style.css      Tampilan
    └── index.js       Logika dan input keyboard
```

---

## Menjalankan

Tidak perlu instalasi. Clone repository, lalu buka `index.html` di browser.

```bash
git clone https://github.com/HaryMuktiRamdhani/Tugas-Calculator.git
cd Tugas-Calculator/"tugas membuat kalkulator"
```

Setelah itu buka berkas `index.html` dengan klik dua kali, atau jalankan server lokal:

```bash
python -m http.server 8000
```

Lalu buka `http://localhost:8000`.

---

## Catatan Teknis

- Ekspresi dievaluasi dengan `eval()`. Ini praktis untuk proyek latihan dan penggunaan lokal, tetapi untuk aplikasi produksi sebaiknya diganti dengan parser ekspresi.
- Operator `%` bekerja sebagai **modulo** (sisa bagi) seperti di JavaScript, bukan persentase. Contoh: `10 % 3` menghasilkan `1`.

---

<div align="center">

Dibuat oleh **Hary Mukti Ramdhani** &nbsp;&middot;&nbsp; [@HaryMuktiRamdhani](https://github.com/HaryMuktiRamdhani)

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,100:2563eb&height=100&section=footer" alt="" width="100%">

</div>
