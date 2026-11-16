# Website Portfolio Andhika Putradhitya — v25

## Isi paket

```
index.html                         — seluruh situs (CSS, JS, thumbnail, CV ter-embed)
assets/video/showcase.mp4          — showreel hero, 5,0 MB
assets/video/tsof-trailer.mp4      — trailer blok sorotan The Soul of Founder, 1,1 MB
assets/video/kahf-imx_v1.mp4       — Tanya Kahf Bro (IMX), 5,0 MB
assets/video/kahf-imx_v2.mp4       — Tanya Kahf Bro (IMX), 3,6 MB
assets/img/kahf/*.webp             — 24 gambar bukti Paragon (tile + penampil), resolusi penuh
assets/img/xp/*.webp               — 7 gambar kartu Track Record, 1800 px
```

**Seluruh folder harus ikut.** Deploy: `vercel --prod` dari dalam folder ini
(pilih *Link to existing project*), atau seret folder ke app.netlify.com/drop.

## Perubahan v25

- **Pulau berjarak 12 px** ("air" selebar 12 px di antara keping), bentuk
  gabungannya tetap satu persegi utuh; jembatan titik-titik menyeberangi air.
- **Hover:** hanya pulau yang disentuh kursor (beserta labelnya) mengambang
  ringan dan bergoyang kecil, dengan bayangan; kembali saat kursor pergi.
  Di mode kurangi-gerak cuma terangkat 4 px tanpa goyang.
- **YOU'RE HERE** sekarang tepat di sebelah pin LV 4.
- **Ukuran keempat pulau berbeda.** Tata letak jadi dua kolom (kiri LV1/LV4,
  kanan LV2/LV3) dengan garis pantai yang tingginya beda tiap kolom. Bobot:
  1 karya = 1, 1 peran = 2, 1 bukti (klip/foto) = 0,5; luas ∝ bobot^0,6.
  Hasil: 2023 (28) > 2026 (19) > 2025 (7) > 2024 (6).

## Perubahan v24

Roadmap jadi **puzzle pulau**: empat keping dengan garis pantai bergelombang
dan satu tab puzzle di tiap sambungan; digabung jadi satu persegi utuh. Luas
keping tetap mengikuti bobot tahun (karya + peran + bukti), tapi angkanya
tidak lagi ditampilkan. Tiap keping beda nada warna. Jalur antar-level jadi
"jembatan" titik-titik yang menyeberang di tab puzzle — semuanya sama persis:
panjang 56 px, 5 titik, satu penanda kuning di ujung. Di layar sempit keping
berubah jadi empat pita bertumpuk dengan aturan yang sama.

## Perubahan v23

1. **Halaman Paragon jadi satu kotak per sorotan, bukti diutamakan.** Teks di
   kolom kiri yang ramping, galeri di kanan dengan kartu setinggi panel
   (±490 px di desktop, sebelumnya ±170 px). Halaman sebelum/sesudah hanya
   mengintip tipis — efek drum 3D tetap ada.
2. **Tidak ada lagi yang menutupi wajah.** Tombol play besar di tengah diganti
   ikon kecil di sudut kanan-bawah; keterangan dan angka (260K+ dst.) pindah
   ke bawah gambar. Ukuran kartu dihitung dari ruang yang tersedia, gambar
   melebar dikecilkan sampai muat utuh — tidak ada yang dipotong paksa.
3. **ASEAN Cup:** tile Instagram sekarang memakai gambar slide 2 itu sendiri,
   tanpa tulisan "slide 2".
4. **Foto tidak pecah lagi.** Penyebabnya: tile memakai thumbnail 360 px yang
   ditanam di HTML lalu diperbesar 2–3×. Sekarang tiap tile memakai file
   resolusi penuh (foto 1600 px, cover TikTok 1280 px) yang diambil lebih
   dulu saat halaman menganggur. Kartu Track Record juga naik dari 900 px ke
   1800 px. Bonus: HTML turun dari 3,2 MB ke 2,3 MB.
5. **Roadmap jadi papan level ala game.** Baris 1 kiri→kanan, turun, baris 2
   kanan→kiri, disambung jalur titik-titik; mengisi lebar kolom. Lebar dan
   ukuran huruf tiap kotak = bobot tahun itu di portofolio (karya + peran +
   bukti), dihitung otomatis dari data:

   | Tahun | Isi | Bobot |
   |---|---|---|
   | 2023 | 22 karya · 3 peran | 25 |
   | 2024 | 6 karya | 6 |
   | 2025 | 5 karya · 1 peran | 6 |
   | 2026 | 1 karya · 3 peran · 24 bukti | 28 |

## Perubahan v22

### 1. ParagonCorp masuk Track Record — dengan pager 3D

Kartu pertama di Track Record sekarang ParagonCorp (Social Media Management
Intern, Kahf · Sep 2026 — Present), thumbnail kolase Kahf. Kartunya bertuliskan
"Explore 4 highlights".

Saat dibuka, panelnya tidak berisi daftar poin biasa tapi **empat halaman
bertumpuk vertikal** — satu halaman per poin CV:

| # | Halaman | Media |
|---|---|---|
| 01 | 11.11 LIVE push · Super Brand Day | 3 TikTok (260K+ / 200K+ / 100K+) + 1 foto |
| 02 | On-ground activations | 4 grup: IMX 2026 (2 video, 3 foto) · Shake-Out Run (2) · Kahf x BYON (4) · ASEAN Cup (IG + 2) |
| 03 | Kahf x BYON · Road to Grand Prix 2026 | 3 TikTok |
| 04 | Content pipeline | 3 key visual / brief |

Perilakunya:

- Halaman aktif di tengah; halaman sebelumnya mengintip di atas dan halaman
  berikutnya di bawah, **opacity rendah dan miring menjauh** (`rotateX` dengan
  `perspective`) — efek drum 3D.
- Tombol **panah bawah** berlabel "Next highlight · 2 / 4" + judul halaman
  berikutnya, chevron yang memantul, dan cincin berdenyut sampai pengguna
  pertama kali berpindah halaman. Ada juga tombol atas, rel titik di kanan,
  dan halaman yang mengintip bisa diklik langsung.
- Pindah halaman: halaman bawah **naik ke tengah sambil opacity-nya penuh**
  (0,82 detik).
- Juga bisa lewat keyboard (↓ ↑ PageDown PageUp), roda mouse, dan usap di
  layar sentuh. Roda/usap baru membalik halaman setelah isi halaman mentok;
  satu kibasan trackpad = satu halaman (diuji: sebelum perbaikan kunci
  inersia, satu kibasan melompati 3 halaman).
- Klik media → penampil di dalam panel: TikTok (player resmi), video lokal,
  foto ukuran penuh, embed Instagram, dengan tombol "Open original".
  Esc menutup penampil dulu, baru panelnya.

Peran lain tetap memakai panel teks biasa.

### 2. Disamakan dengan CV terbaru

- CV baru tertanam; CV lama tidak tersisa (tepat 1 PDF di berkas).
- Summary = summary CV, kata per kata.
- Hero: chip **Social Media Management** + "Content calendars, campaign briefs
  & talent-led content". Chip foto: Social Media · Media Production · Art Direction.
- `<title>`, meta description, og:description, keywords, dan JSON-LD
  (`jobTitle`, `worksFor: ParagonCorp`, `knowsAbout`).
- Pendidikan: + *Relevant coursework: Social Media, Advertising Content
  Production, Transmedia*.
- Technical skills = daftar di CV.
- Wording MAP Active (KOL pool Back to School/Agustus/September; urutan poin
  desain), OB Golf, dan Transvision disamakan dengan CV.
- "Seven roles since 2023", statistik "Teams & companies" 6 → 7.

### 3. Kedipan thumbnail dihilangkan

Penyebab: kartu menampilkan poster lama dulu, lalu menukarnya dengan
thumbnail Drive/YouTube begitu termuat. Sekarang thumbnail final itu yang
ditanam langsung saat build — **28 kartu Works, 6 kartu Track Record, 2 gambar
MedEdu**. Tidak ada penukaran di browser.

Diuji: **0 permintaan** ke googleusercontent / drive thumbnail / ytimg saat
halaman dibuka. Efek samping yang bagus: thumbnail tidak lagi bergantung pada
permission folder Drive.

### 4. Dibangun ulang di atas situs live

Situs live ternyata masih build v18/v19; v20 dan v21 belum pernah ter-deploy.
v22 dibangun ulang di atas berkas live dengan menerapkan ulang seluruh
perubahan v20 dan v21 (blok sorotan TSOF + trailer, angka 3.9M, perbaikan
urutan pause video, teks galat Inggris).

## Hasil uji

Chrome headless, 1440px dan 390px: **0 error JavaScript**, 35 karya,
7 kartu Track Record (semua gambar ter-embed), 0 overflow horizontal, pager
4 halaman berpindah benar lewat tombol, keyboard, dan roda mouse; penampil
TikTok/foto/video terbuka dan tertutup benar.
