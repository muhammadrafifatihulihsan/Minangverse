
# 📟 Minangverse
Minangverse platform literasi budaya interaktif sebagai media edukasi dan ekspresi untuk memajukan budaya Indonesia yang mengangkat budaya Minangkabau melalui teknologi web. Dengan fitur alat musik virtual yang dapat dimainkan secara realtime, permainan kartu kuis gamified, pepatah, kuis budaya, kamus nasihat hingga galeri interaktif dengan UI bernuansa Minangkabau dengan ciri khas songket. Minangverse menghadirkan pembelajaran budaya yang imersif, edukatif dan menyenangkan bagi generasi digital

# 🌐 Dokumentasi Proyek

## 🔗 URL Aplikasi

**Production / Demo Live (Link Demo)**

https://minangverse-project.vercel.app/

---

**Link Github Project**

https://github.com/muhammadrafifatihulihsan/Minangverse.git

**Local Development**

Frontend (React + Vite): http://localhost:5173

Supabase API: otomatis dari `.env`

---

# 📘 Penjelasan Singkat Aplikasi

Minangverse platform literasi budaya interaktif sebagai media edukasi dan ekspresi untuk memajukan budaya Indonesia yang mengangkat budaya Minangkabau melalui teknologi web. Dengan fitur alat musik virtual yang dapat dimainkan secara realtime, permainan kartu kuis gamified, pepatah, kuis budaya, kamus nasihat hingga galeri interaktif dengan UI bernuansa Minangkabau dengan ciri khas songket. Minangverse menghadirkan pembelajaran budaya yang imersif, edukatif dan menyenangkan bagi generasi digital

---

# ✅ Fitur Inti

1. Landing Page informatif
2. Ringkasan budaya Minangkabau
3. Alat Musik Virtual
4. Kamus Bahasa Minang
5. Kartu Keberuntungan (Funfact budaya)
6. Live Chat Anonim Real-time

---

# ✅ Teknologi Digunakan

1. React + Vite
2. TailwindCSS + DaisyUI
3. Supabase (Auth, DB, Realtime)

---

# 🔐 Demo Credentials

> Saat ini login belum diperlukan.

---

# 📦 Kebutuhan Sebelum Instalasi

### 1. Node.js v18+

https://nodejs.org/en

### 2. Akun Supabase

Untuk fitur: Live Chat.

### 3. Git (opsional)

---

# 📁 Struktur Proyek

```
minangverse/
│
├── client/          # Frontend React + Vite
│   ├── src/
│   ├── public/
│   ├── vite.config.js
│   └── package.json
│
└── server/          # Backend (masih kosong karena menggunakan alternatif, supabase)
```

---

# ⚙️ Instalasi & Menjalankan Proyek (Local)

## 1. Clone Repo

```
git clone https://github.com/muhammadrafifatihulihsan/Minangverse.git
cd Minangverse
```

## 2. Masuk ke frontend

```
cd client
```

## 3. Install dependencies

```
npm install
```

## 4. Siapkan file .env

Buat file `client/.env`:

```
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

Skema Tabel messages
```
create table public.messages (
  id bigserial not null,
  user_id uuid null,
  username text not null,
  content text not null,
  created_at timestamp with time zone null default now(),
  constraint messages_pkey primary key (id)
) TABLESPACE pg_default;

create index IF not exists messages_created_at_idx on public.messages using btree (created_at desc) TABLESPACE pg_default;
```

## 5. Jalankan Aplikasi

```
npm run dev
```

Akses: http://localhost:5173

---

# 🧩 Penjelasan Fitur

## 1. Landing Page

Halaman utama dengan deskripsi fitur dan visual Minangkabau. Alur fungsi: Pengguna membuka halaman utama. Sistem menampilkan hero section, pengantar budaya, tombol navigasi menuju fitur lain. Animasi ringan Tailwind/GSAP digunakan untuk memberikan pengalaman visual yang modern.

## 2. Introduction

Ringkasan budaya Minangkabau dari dasar hingga filosofi. Alur fungsi: Konten budaya (adat, rumah gadang, makanan, sejarah) ditampilkan dalam deskripsi dinamis. Data diambil secara statis dari file. Kemudian pengguna dapat scroll dan membaca ringkasan secara bertahap.

## 3. Alat Musik Virtual

Daftar alat musik, halaman detail, dan mode permainan. Alur fungsi: Pengguna membaca deskripsi penjelasan mengenai alat musik dan memilih alat musik (misalnya talempong). Sistem memuat audio terkait. Ketika pengguna menekan tombol/elemen UI, file audio diputar. React menangani state input interaksi, sementara tailwind memastikan layout responsif.

## 4. Kamus Minang

Pencarian kata, arti, jenis kata, contoh kalimat, dan contoh pengucapan. Alur fungsi: Pengguna mengetik kata Indonesia atau Minang. Sistem melakukan pencarian lokal atau dari Supabase. Hasil pencarian muncul secara real-time dan pengguna dapat mendengarkan cara pengucapan dari contoh kalimat yang diberikan.

## 5. Kartu Keberuntungan

Kartu acak berisi funfact budaya Minangkabau. Alur fungsi: Pengguna membuka halaman kartu. Sistem mengambil daftar funfact dari file data. Kartu muncul bergantian dengan animasi. Setiap klik mengganti kartu secara acak.

## 6. Live Chat Anonim

Chat global real-time tanpa login. Alur fungsi: Ketika pengguna masuk, sistem membuat atau mengambil user anonim dari localStorage. Pesan dikirim ke Supabase Realtime. Listener realtime menangkap pesan baru dari pengguna lain. UI otomatis scroll ke pesan terbaru menggunakan useRef.

---

# 🛠 Teknologi

| Bagian   | Teknologi             |
| -------- | --------------------- |
| Frontend | React + Vite          |
| UI       | TailwindCSS + DaisyUI |
| Database | Supabase              |
| Auth     | Supabase Auth         |
| Realtime | Supabase Realtime     |
| Backend  | —                     |

---

# 🧪 Troubleshooting

**Supabase tidak connect:** cek `.env`, project aktif, API key benar.

**Tailwind tidak muncul:** cek `tailwind.config.js` & `postcss.config.js`.

**Chat tidak realtime:** aktifkan Replication → Realtime di Supabase.

---

# 📬 Kontak

**GitHub:** https://github.com/muhammadrafifatihulihsan

**Email:** [muhammadrafifatihulihsan@gmail.com](mailto:muhammadrafifatihulihsan@gmail.com)

## ✨ Big Thanks
Terima kasih untuk Rafif, Arya, Fitri, dan Zulfa karena sudah benar-benar berusaha, rela begadang, nyempetin waktu di tengah kesibukan, dan tetap semangat buat ngerjain Minangverse sampai jadi seperti sekarang. Aku sangat menghargai setiap usaha kecil maupun besar yang kalian lakukan. Terima kasih sudah sama-sama saling dukung dan nggak nyerah meski capek. Semoga semua lelah dan kerja keras kalian jadi hal yang bernilai dan dibalas dengan kebaikan.

```bash
Tidaklah seorang tertimpa kelelahan, sakit, kesedihan, kesusahan, gangguan, ataupun kegelisahan bahkan duri yang menusuknya kecuali Allah akan menghapuskan sebagian dosa-dosanya. HR. Bukhari dan Muslim
```
## 🤡 Authors
- [@rafiiee](https://github.com/muhammadrafifatihulihsan)
- [@rafif](https://github.com/cawfe2526)
- [@Arya](https://github.com/#)
- [@Fitri](https://github.com/#)
- [@Zulfa](https://github.com/#)

