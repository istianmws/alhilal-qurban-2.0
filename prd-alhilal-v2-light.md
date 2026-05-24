# PRD v2.0 — Landing Page Idul Adha 1447H
## Masjid Al-Hilal Donorejo · "Berkurban, Bahagiakan Sesama"
### Revisi: Light Mode — Krem/Ivory Hangat + Aksen Hijau-Oranye

---

## 1. Perubahan dari v1.0

| Aspek | v1.0 (Dark Glassmorphism) | v2.0 (Light Ivory) |
|---|---|---|
| Background | Hijau tua gelap (#0a2e1a) | Ivory/krem hangat (#FAF6EF) |
| Nuansa | Masjid malam hari, mistis | Siang yang hangat, bersih, ramah |
| Card style | Glass transparan gelap | Putih bersih dengan shadow soft |
| Target feel | Elegan premium | Hangat, approachable, modern |
| Teks utama | Putih kehijau-hijauan | Coklat tua (#2D1E0F) |

---

## 2. Design System v2.0

### Palet Warna

| Token | Hex | Penggunaan |
|---|---|---|
| `--bg-base` | `#FAF6EF` | Background utama halaman |
| `--bg-warm` | `#F5EFE3` | Background section alternating |
| `--bg-card` | `#FFFFFF` | Surface kartu & komponen |
| `--green-primary` | `#2D7A4F` | Aksen utama, CTA, heading accent |
| `--green-light` | `#4CAF75` | Hover, highlight, badge |
| `--green-pale` | `#E8F5EE` | Background badge, tag, pill |
| `--orange-primary` | `#E07840` | Aksen sekunder, angka besar, highlight |
| `--orange-light` | `#F5A66B` | Badge, label, dekoratif |
| `--orange-pale` | `#FDF0E6` | Background badge oranye, card accent |
| `--text-heading` | `#1E1206` | Judul utama (Playfair Display) |
| `--text-body` | `#4A3728` | Teks paragraf |
| `--text-muted` | `#9C8070` | Label, caption, placeholder |
| `--border` | `rgba(45,122,79,0.12)` | Border halus kartu |
| `--shadow-sm` | `0 2px 12px rgba(45,50,40,0.07)` | Shadow kartu normal |
| `--shadow-md` | `0 8px 32px rgba(45,50,40,0.12)` | Shadow card hover/featured |
| `--gold` | `#C4902A` | Ayat Al-Quran, ornamen, milestone |

### Tipografi

| Elemen | Font | Weight | Ukuran |
|---|---|---|---|
| Hero Title | Playfair Display | 900 | clamp(2.4rem, 7vw, 4.8rem) |
| Section Title | Playfair Display | 700 | clamp(1.6rem, 4vw, 2.4rem) |
| Sub-heading | Plus Jakarta Sans | 700 | 1.1–1.25rem |
| Body | Plus Jakarta Sans | 400–500 | 0.9–1rem |
| Badge/Label | Plus Jakarta Sans | 700 | 0.72–0.8rem |
| Arabic (Ayat) | Scheherazade New / serif | 600 | clamp(1.4rem, 4vw, 2rem) |

### Dekorasi & Ornamen

- **Geometric Islamic pattern** — SVG bintang 8 sudut, opacity sangat rendah (0.05–0.08), warna hijau tua, sebagai background texture di section hero dan penutup
- **Floating shapes** — blob/circle organik berwarna `--green-pale` dan `--orange-pale` di hero sebagai elemen dekoratif (mirip referensi FastDeli dengan circle kuning)
- **Garis bawah ornamental** — divider tipis dengan motif geometris islami kecil di tengah
- **Leaf/arabesque SVG** — satu-dua elemen kecil melayang di hero corner (subtle, tidak berlebihan)
- **Dot pattern** — grid titik-titik kecil opacity rendah di beberapa section

---

## 3. Struktur Halaman & Detail Komponen

### NAV
- Background: `rgba(250,246,239,0.85)` + `backdrop-filter: blur(16px)`
- Border bawah: `1px solid rgba(45,122,79,0.1)`
- Logo: "☽ Al-Hilal" — Playfair Display, warna `--green-primary`
- Link: Plus Jakarta Sans 600, `--text-body`
- Sticky dengan scroll shadow yang muncul saat di-scroll

---

### SECTION 1 — HERO
**Layout:** 2 kolom (teks kiri, visual kanan) di desktop; 1 kolom di mobile

**Kolom Kiri:**
- Badge pill: "🌙 Idul Adha 1447 H" — background `--green-pale`, teks `--green-primary`
- H1: "Masjid Al-Hilal" — Playfair Display 900, `--text-heading`
- Tagline: *"Berkurban, Bahagiakan Sesama"* — italic, `--orange-primary`
- Sub: "Ranting Muhammadiyah Donorejo · Desa kecil dengan semangat besar"
- CTA Primary: "🐄 Daftar Qurban" — bg `--green-primary`, rounded-full, shadow hangat
- CTA Secondary: "Lihat Pencapaian ↓" — border `--green-primary`, text `--green-primary`

**Kolom Kanan (Visual):**
- Lingkaran besar `--orange-pale` / `--green-pale` sebagai backdrop (mirip referensi)
- SVG masjid / bulan sabit / ornamen islami yang clean dan berwarna warm
- Floating badge card "🏆 4 Tahun Berturut-turut" — card putih, shadow, muncul melayang
- Floating badge card "🐄 10 Sapi · 🐑 13 Kambing" — card putih melayang
- Elemen dekoratif kecil: daun/bintang SVG di sudut

**Background Hero:**
- Base `--bg-base`
- Radial gradient sangat soft: hijau pale di kiri bawah, oranye pale di kanan atas
- Pattern bintang islami opacity 0.05

---

### SECTION 2 — STATS BESAR
**Background:** `--bg-warm` (krem sedikit lebih gelap)

**Layout:** 2 kartu besar + 1 banner milestone full-width

**Stat Card:**
- Background: `--bg-card` (putih)
- Shadow: `--shadow-md`
- Border radius: 24px
- Border kiri: 4px solid `--green-primary` (sapi) / `--orange-primary` (kambing)
- Angka: font Playfair 900, warna `--green-primary` / `--orange-primary`
- Counter animasi scroll-triggered

**Milestone Banner:**
- Background: gradient `--orange-pale` ke `--green-pale`
- Border: `1px solid rgba(196,144,42,0.25)`
- Border radius: 20px
- Icon 🏆 besar di kiri
- Teks bold `--gold`

---

### SECTION 3 — TREN CHART
**Background:** `--bg-base`

**Chart Card:**
- Background: `--bg-card`
- Shadow: `--shadow-sm`
- Border radius: 20px
- Border top: 3px solid `--green-primary`
- Chart.js Bar grouped — warna bar: `--green-primary` & `--orange-primary`
- Grid lines: `rgba(45,122,79,0.08)`
- Tooltip: background `--text-heading`, rounded

---

### SECTION 4 — CARA BERQURBAN
**Background:** `--bg-warm`

**Layout:** 2 kartu sejajar

**Qurban Card:**
- Background: `--bg-card`
- Shadow: `--shadow-sm`
- Border radius: 20px
- Icon emoji besar + judul Playfair
- Sapi: border top `--green-primary`, badge "⚡ Kuota Terbatas" bg `--orange-pale`
- Kambing: border top `--orange-primary`, badge "✓ Tersedia" bg `--green-pale`
- Row detail: bg alternating `--bg-warm`, border-bottom `--border`

---

### SECTION 5 — JADWAL
**Background:** `--bg-base`

**Timeline Vertikal:**
- Dot: bg `--green-pale`, border `--green-primary`, icon emoji
- Connector line: `--green-light` opacity 0.3, dashed
- Card per item: bg `--bg-card`, shadow `--shadow-sm`, border-left `--green-primary`
- Time label: badge pill `--orange-pale`, teks `--orange-primary`

---

### SECTION 6 — DONASI & PENDAFTARAN
**Background:** `--bg-warm`

**Layout:** 2 kartu

**Kartu Rekening:**
- Header icon bank + "Transfer Bank"
- Nomor besar Playfair: `7777 556 589` warna `--green-primary`
- Divider tipis
- QRIS placeholder: border dashed `--green-light`, bg `--green-pale`

**Kartu WhatsApp:**
- 3 tombol WA: bg `--green-pale`, border `rgba(45,122,79,0.2)`, hover bg `--green-primary` warna putih
- Ikon WA: lingkaran hijau
- Alamat box: bg `--orange-pale`, border `rgba(224,120,64,0.2)`

---

### SECTION 7 — GALERI
**Background:** `--bg-base`

**Grid:**
- 3 kolom, item pertama span 2
- Card placeholder: bg `--bg-card`, shadow `--shadow-sm`
- Border: `1px solid var(--border)`
- Hover: lift effect (translateY -4px) + shadow lebih dalam

---

### SECTION 8 — PENUTUP / QUOTE
**Background:** Gradient `--green-primary` → `#1a5a36` (satu-satunya section dark, sebagai penutup yang impactful)

**Quote Box:**
- Background: `rgba(255,255,255,0.1)` di atas bg gelap
- Teks Arab: `--gold`
- Teks terjemah: putih opacity 0.85
- CTA Button: bg `--orange-primary`, rounded-full

**Footer:**
- Teks: putih opacity 0.55
- Org: `--green-soft` opacity 0.8

---

## 4. Animasi & Interaksi

| Elemen | Animasi |
|---|---|
| Semua section | Fade-in + slide-up on scroll (IntersectionObserver) |
| Stat numbers | Count-up 0 → target, ease-out cubic |
| Hero floating cards | Float up-down gentle (CSS keyframe, 3–4s) |
| Nav | Shadow muncul saat scroll > 50px |
| Kartu | translateY(-4px) + shadow lebih dalam on hover |
| CTA button | Scale(1.02) + shadow on hover |
| WA button | translateX(4px) on hover |

---

## 5. Responsif Breakpoints

| Breakpoint | Layout |
|---|---|
| > 900px | Hero 2 kolom, grid 2 kolom, galeri 3 kolom |
| 600–900px | Hero 1 kolom (visual di bawah), grid 2 kolom |
| < 600px | Semua 1 kolom, nav collapse (hide links) |
| < 380px | Font lebih kecil, padding dikurangi |

---

## 6. Placeholder Yang Perlu Diisi

- [ ] Nama pemilik rekening BSI 7777 556 589
- [ ] Gambar QRIS asli (ganti `<div class="qris-placeholder">`)
- [ ] 5 foto dokumentasi (ganti `.g-item` placeholder)
- [ ] Nominal estimasi biaya sapi & kambing per orang
- [ ] Tanggal & jam jadwal pasti (saat ini pakai estimasi)

---

## 7. File Output

- Single file `alhilal-iduladha-v2.html` (HTML + CSS + JS inline)
- Chart.js via CDN cdnjs
- Google Fonts: Playfair Display + Plus Jakarta Sans
- Zero dependencies selain CDN di atas
- Deploy: drag & drop ke Vercel — done ✅

---

*PRD v2.0 — Light Ivory Edition — siap untuk implementasi*
