# Uji Kompetensi BNSP — HVAC & Refrigerasi

Aplikasi ujian kompetensi online dengan koreksi AI untuk soal essay.

---

## 📁 Struktur File

```
uji-kompetensi/
├── index.html                    ← Halaman utama
├── vercel.json                   ← Konfigurasi Vercel
├── netlify.toml                  ← Konfigurasi Netlify
├── api/
│   └── claude.js                 ← Serverless function (Vercel)
└── netlify/
    └── functions/
        └── claude.js             ← Serverless function (Netlify)
```

---

## 🚀 Deploy ke Vercel (Direkomendasikan)

### Langkah 1: Upload ke GitHub
1. Buat repository baru di [github.com](https://github.com)
2. Upload semua file ini ke repository tersebut

### Langkah 2: Deploy di Vercel
1. Buka [vercel.com](https://vercel.com) → Login
2. Klik **"New Project"** → Import repository GitHub Anda
3. Klik **"Deploy"** (tanpa mengubah settings apapun)

### Langkah 3: Tambahkan API Key
1. Di dashboard Vercel project Anda → **Settings** → **Environment Variables**
2. Tambahkan:
   - **Name:** `KIMI_API_KEY`
   - **Value:** API key Anda dari [platform.moonshot.cn](https://platform.moonshot.cn)
3. Klik **Save**, lalu **Redeploy** project

✅ Selesai! Website Anda sudah online.

---

## 🚀 Deploy ke Netlify (Alternatif)

### Langkah 1: Upload ke GitHub
Sama seperti langkah Vercel di atas.

### Langkah 2: Deploy di Netlify
1. Buka [netlify.com](https://netlify.com) → Login
2. Klik **"Add new site"** → **"Import an existing project"**
3. Pilih repository GitHub Anda
4. **Publish directory:** `.` (titik, artinya root folder)
5. Klik **"Deploy site"**

### Langkah 3: Tambahkan API Key
1. Di dashboard Netlify → **Site configuration** → **Environment variables**
2. Tambahkan:
   - **Key:** `KIMI_API_KEY`
   - **Value:** API key Anda
3. Klik **Save**, lalu **Trigger deploy** → **Deploy site**

---

## 🔑 Mendapatkan API Key Anthropic

1. Buka [console.anthropic.com](https://console.anthropic.com)
2. Login / daftar akun
3. Klik **"API Keys"** → **"Create Key"**
4. Copy key tersebut → paste ke environment variable

---

## ❓ Kenapa perlu API Key?

Aplikasi ini menggunakan AI Claude untuk mengoreksi jawaban essay secara otomatis. API key diperlukan agar server bisa berkomunikasi dengan layanan AI Anthropic. API key **tidak akan terlihat** oleh pengguna karena disimpan di server (environment variable), bukan di dalam kode HTML.

---

## 🌐 Fitur Aplikasi

- ✅ 30 soal pilihan ganda (diacak)
- ✅ 5 soal essay per ujian
- ✅ Timer 90 menit
- ✅ Koreksi AI otomatis untuk jawaban essay
- ✅ Review jawaban lengkap setelah ujian
- ✅ Dua materi: Mekanik HVAC & Teknisi Refrigerasi
- ✅ Standar kompetensi BNSP / SKKNI
