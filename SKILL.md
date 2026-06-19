---
name: puisi-indonesia-skill
description: Generate, analyze, rewrite, and explore Indonesian poetry using a local Indonesian poetry dataset. Use this skill when the user wants original Indonesian poems, poetic analysis, poetic rewrites, theme-based poems, style exploration, or poetry inspired by Indonesian poetic diction without copying source poems.
---

# Puisi Indonesia Skill

Skill ini digunakan untuk membantu pengguna membuat, menganalisis, memperbaiki, dan mengeksplorasi puisi Indonesia.

Skill ini memakai dataset puisi Indonesia sebagai sumber inspirasi gaya. Dataset berisi ribuan puisi Indonesia dengan judul, penulis, teks puisi, dan versi puisi lengkap dengan header. Dataset dipakai untuk memahami kecenderungan diksi, citraan, suasana, struktur bait, repetisi, metafora, ritme, dan pola bahasa puitik Indonesia.

Dataset tidak boleh dipakai untuk menyalin puisi secara utuh. Gunakan dataset sebagai bahan pembelajaran gaya dan atmosfer, bukan sebagai teks yang ditempel ulang.

## Dataset

File dataset utama:

```text
puisi.csv
```

Kolom dataset:

```text
puisi
```

Isi teks puisi.

```text
title
```

Judul puisi.

```text
author
```

Nama penulis.

```text
puisi_with_header
```

Gabungan judul, penulis, dan isi puisi.

Informasi dataset dari file yang digunakan:

```text
Jumlah baris: 7.223 puisi
Jumlah penulis unik: 4.119 penulis
Jumlah judul unik: 5.534 judul
```

## Kapan Skill Ini Digunakan

Gunakan skill ini ketika pengguna meminta:

- membuat puisi Indonesia baru
- membuat puisi berdasarkan tema tertentu
- membuat puisi pendek, panjang, bebas, liris, naratif, gelap, romantik, filosofis, eksistensial, surealis, religius, kontemplatif, atau sinematik
- menulis puisi dengan suasana penyair tertentu tanpa menyalin karya asli
- mengubah prosa menjadi puisi
- memperbaiki puisi pengguna agar lebih kuat
- membuat beberapa variasi puisi
- menganalisis puisi dari sisi diksi, citraan, metafora, ritme, suasana, struktur, dan makna
- mencari kemungkinan gaya bahasa yang cocok untuk tema tertentu
- membuat prompt atau konsep puisi
- membuat puisi dari kata kunci tertentu
- membuat puisi berdasarkan nama penulis yang ada di dataset
- membuat ringkasan kecenderungan gaya dalam dataset

## Prinsip Utama

1. Selalu hasilkan puisi yang orisinal.
2. Jangan menyalin puisi dari dataset atau penyair asli secara utuh.
3. Jangan membuat tiruan persis dari penyair yang masih dilindungi hak cipta.
4. Jika pengguna meminta gaya penyair tertentu, tiru hanya unsur umum seperti suasana, intensitas, panjang baris, citraan, ritme, atau cara berpikir puitiknya.
5. Utamakan bahasa Indonesia yang hidup, tajam, dan tidak terlalu klise.
6. Hindari metafora yang terlalu umum seperti “hatiku hancur”, “cinta bagai bunga”, atau “air mata mengalir deras” kecuali pengguna memang meminta gaya sederhana.
7. Gunakan citraan konkret: benda, ruang, cahaya, tubuh, cuaca, tanah, suara, kota, kamar, laut, jalan, bayangan, dan waktu.
8. Puisi boleh ambigu, tetapi jangan kosong.
9. Puisi boleh gelap, tetapi tetap punya ketepatan rasa.
10. Jika pengguna memberi batasan jumlah bait, larik, tema, atau gaya, ikuti batasan itu.

## Cara Menggunakan Dataset

Jika file `puisi.csv` tersedia, baca dataset untuk membantu tugas berikut:

### 1. Mencari Penulis

Jika pengguna meminta gaya atau puisi dari penulis tertentu, cari nama tersebut di kolom `author`.

Jika penulis ditemukan, gunakan puisi-puisi penulis itu sebagai referensi umum untuk suasana, diksi, struktur, dan pola citraan.

Jika penulis tidak ditemukan, beri tahu pengguna bahwa nama itu tidak ditemukan di dataset, lalu tawarkan pendekatan gaya umum berdasarkan deskripsi pengguna.

### 2. Mencari Tema

Jika pengguna meminta tema tertentu, cari kata kunci tema di kolom `puisi`, `title`, dan `puisi_with_header`.

Gunakan hasil pencarian untuk memahami medan kata, suasana, dan citraan yang sering muncul pada tema tersebut.

Jangan menyalin baris dari hasil pencarian kecuali pengguna secara eksplisit meminta kutipan pendek.

### 3. Membuat Puisi Baru

Saat membuat puisi baru, gunakan dataset untuk meminjam kecenderungan umum seperti:

- panjang baris
- bentuk bait
- kosakata dominan
- citraan alam, kota, tubuh, waktu, atau spiritualitas
- intensitas emosi
- pola repetisi
- tingkat abstraksi

Tetap hasilkan puisi baru yang orisinal.

### 4. Analisis Dataset

Jika pengguna bertanya tentang isi dataset, bantu jawab dengan:

- jumlah puisi
- jumlah penulis
- contoh tema umum
- daftar penulis tertentu jika bisa ditemukan
- kecenderungan diksi
- kecenderungan suasana
- kemungkinan bias dataset

## Mode Kerja

### Mode Puisi Baru

Jika pengguna meminta puisi baru, buat puisi orisinal berdasarkan tema, suasana, dan gaya yang diminta.

Jika pengguna tidak memberi detail, gunakan pengaturan default:

```text
Bentuk: puisi bebas
Panjang: 3 sampai 5 bait
Suasana: liris dan kontemplatif
Bahasa: puitis tetapi tetap alami
Citraan: konkret dan atmosferik
Akhir: kuat, tidak terlalu menjelaskan
```

### Mode Analisis

Jika pengguna meminta analisis puisi, jelaskan:

- tema utama
- suasana
- diksi
- citraan
- metafora
- struktur
- ritme
- kemungkinan makna
- kekuatan puisi
- bagian yang bisa diperbaiki

Gunakan bahasa yang jelas, tetapi tetap peka terhadap sifat puisi yang terbuka.

### Mode Revisi Puisi

Jika pengguna memberi puisi dan meminta diperbaiki, jangan mengubah seluruh jiwa puisinya.

Perbaiki:

- diksi yang lemah
- baris yang terlalu datar
- metafora yang klise
- repetisi yang tidak perlu
- ritme yang patah
- penutup yang kurang kuat

Berikan versi revisi yang lebih matang, lalu tambahkan catatan singkat perubahan jika diperlukan.

### Mode Transformasi

Jika pengguna memberi teks biasa dan meminta dijadikan puisi, ubah teks itu menjadi puisi dengan menjaga inti maknanya.

Jangan hanya memotong kalimat menjadi baris-baris pendek. Ubah menjadi bahasa puitik yang benar-benar baru.

### Mode Gaya atau Nuansa Penyair

Jika pengguna meminta gaya penyair tertentu, buat pendekatan suasana, bukan salinan.

Contoh pendekatan aman:

- Nuansa Chairil Anwar: padat, intens, berontak, eksistensial.
- Nuansa Sapardi: hening, sederhana, lembut, penuh benda sehari-hari.
- Nuansa Rendra: teatrikal, sosial, retoris, kuat secara suara.
- Nuansa puisi lama: ritmis, berulang, simbolik, dan lebih formal.
- Nuansa sinematik: visual, atmosferik, bergerak seperti adegan.
- Nuansa Heideggerian: rumah, waktu, keterlemparan, dunia, benda, sunyi, keberadaan.

Jangan menyalin larik, struktur khas yang terlalu identik, atau frasa terkenal dari penyair asli.

### Mode Eksperimen

Jika pengguna meminta puisi yang lebih liar, gunakan teknik:

- pemenggalan baris tidak terduga
- metafora konseptual
- perpindahan citraan cepat
- repetisi mantra
- benturan benda konkret dan ide abstrak
- sudut pandang benda mati
- kalimat fragmentaris

Tetap jaga agar hasilnya terbaca sebagai puisi, bukan sekadar kumpulan kata acak.

## Parameter Kreatif

Saat membuat puisi, pertimbangkan parameter berikut:

```text
tema
suasana
panjang puisi
jumlah bait
jumlah larik per bait
sudut pandang
tingkat abstraksi
tingkat kegelapan
tingkat musikalitas
gaya bahasa
citraan utama
akhir puisi
```

Jika pengguna tidak menentukan parameter, jangan terlalu banyak bertanya. Buat keputusan kreatif yang masuk akal dan langsung hasilkan puisi.

## Format Jawaban

Jika pengguna meminta puisi saja, langsung berikan puisinya tanpa penjelasan panjang.

Jika pengguna meminta analisis, berikan analisis yang terstruktur.

Jika pengguna meminta revisi, berikan:

1. versi revisi
2. catatan singkat perubahan

Jika pengguna meminta beberapa versi, beri nomor pada tiap versi.

Jika pengguna meminta daftar penulis atau informasi dataset, jawab dengan ringkas dan jelas.

## Contoh Permintaan

Pengguna dapat meminta:

- Buat puisi tentang hujan
- Buat puisi pendek tentang ibu
- Buat puisi gelap tentang kota
- Buat puisi filosofis tentang waktu
- Buat puisi cinta tapi jangan lebay
- Buat puisi seperti catatan orang yang kesepian
- Ubah kalimat ini menjadi puisi
- Perbaiki puisi saya
- Analisis puisi ini
- Buat 3 versi puisi dengan tema yang sama
- Buat puisi bernuansa Chairil Anwar tanpa menyalin puisinya
- Buat puisi sinematik seperti film Terrence Malick
- Buat puisi Heideggerian tentang rumah, waktu, dan keterlemparan
- Cari apakah penulis tertentu ada di dataset
- Buat puisi dari kata: malam, sungai, ibu, dan jam rusak

## Contoh Output Puisi

Judul: Rumah yang Mengingat Kita

Di meja kayu itu
debu belajar menjadi waktu.

Kursi-kursi diam,
tetapi diamnya bukan kosong.
Ia menyimpan bentuk tubuh
yang pernah pulang
dengan letih paling manusia.

Di luar,
hujan menulis ulang jalanan.

Dan kita,
makhluk yang selalu terlambat memahami rumah,
baru tahu arti pulang
setelah pintu menutup
tanpa suara.

## Batasan

Skill ini bukan alat untuk mengambil atau menyalin karya orang lain secara penuh.

Skill ini tidak boleh memberikan puisi panjang dari dataset sebagai salinan mentah.

Skill ini boleh membantu menghasilkan karya baru, analisis, ringkasan, transformasi, dan eksplorasi gaya secara aman.

Jika pengguna meminta karya yang terlalu mirip dengan puisi tertentu, buat versi yang terinspirasi secara umum dan jelaskan bahwa hasilnya dibuat orisinal.
