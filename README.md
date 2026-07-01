<div align="center">

# Website Pascasarjana Ilmu Komputer IPB University
### *Company Profile & Academic Information System*

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](#)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](#)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](#)
[![PHP](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white)](#)
[![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)](#)
[![WordPress](https://img.shields.io/badge/WordPress-21759B?style=for-the-badge&logo=wordpress&logoColor=white)](#)

**Status Proyek:** `Production` &nbsp;|&nbsp; **Skala:** `60+ Halaman` &nbsp;|&nbsp; **Peran:** `Front-End Developer & Web Administrator`

</div>

---

## Confidentiality Notice

> **PERINGATAN KERAHASIAAN (CONFIDENTIALITY NOTICE)**
>
> Repositori ini merupakan **dokumentasi tugas** yang disusun untuk kepentingan demonstrasi pengumpulan tugas. Mengingat proyek ini dikembangkan dan dioperasikan secara langsung pada **server produksi (production environment)** milik Sekolah Pascasarjana Ilmu Komputer, IPB University, maka:
>
> 1. **Source code inti** (PHP core, child-theme functions, custom plugin), **file konfigurasi server** (`.htaccess`, `wp-config.php`, environment variables), serta **skema/dump database (MySQL)** **tidak disertakan** dan **tidak akan dipublikasikan** dalam repositori ini.
> 2. Seluruh kredensial akses, endpoint internal, dan data pengguna/mahasiswa bersifat rahasia dan dilindungi oleh kebijakan institusi.
> 3. Konten dalam repositori ini **murni bersifat deskriptif-teknis**, berfokus pada pemaparan **Arsitektur Informasi**, **UI/UX Design Decision**, dan **implementasi kustomisasi Front-End tingkat lanjut** yang dikerjakan secara langsung oleh tim Capstone-28.
> 4. Cuplikan kode (*code snippet*) yang ditampilkan pada dokumen ini adalah **contoh ilustratif** dari teknik yang diterapkan, bukan salinan langsung dari basis kode produksi.

---

## Deskripsi Proyek

Proyek ini merupakan pengembangan dan pemeliharaan **website resmi Sekolah Pascasarjana Ilmu Komputer, IPB University**, yang berfungsi sebagai *company profile* institusi sekaligus **sistem informasi akademik** bagi calon mahasiswa, mahasiswa aktif, dan alumni program studi S2 dan S3 Ilmu Komputer.

Dibangun di atas platform **WordPress 7.0** dengan basis tema **Mitech**, situs ini dikelola dalam skala menengah-besar dengan lebih dari **60 halaman terstruktur**, mencakup profil, informasi akademik, admisi, kemahasiswaan, hingga berita.

Fokus utama kontribusi teknis pada proyek ini terletak pada **rekayasa Front-End tingkat lanjut**, khususnya dalam menyelaraskan keterbatasan *page builder* (WPBakery) dengan standar desain *pixel-perfect* dan responsivitas lintas perangkat.

---

## Tumpukan Teknologi (Tech Stack)

| Kategori | Teknologi | Fungsi Implementasi |
|---|---|---|
| **Markup & Styling** | HTML5, CSS3 | Struktur semantik & kustomisasi visual tingkat lanjut |
| **Scripting** | JavaScript | Interaktivitas komponen UI & manipulasi DOM |
| **Server-Side** | PHP | Logika backend & integrasi tema WordPress |
| **Basis Data** | MySQL | Penyimpanan konten & data transaksional situs |
| **CMS Platform** | WordPress 7.0 (Tema: Mitech) | Fondasi pengelolaan konten institusi |
| **Page Builder** | WPBakery Page Builder | Konstruksi tata letak halaman secara modular |
| **Visual Engine** | Slider Revolution | Slider dinamis pada halaman beranda & landing page |
| **Navigasi** | Mega Menu | Struktur navigasi hierarkis untuk 60+ halaman |
| **SEO** | Yoast SEO | Optimasi metadata, sitemap XML, dan keterbacaan mesin pencari |
| **Backup & Recovery** | UpdraftPlus | Manajemen backup terjadwal & disaster recovery |
| **Internal Linking** | Internal Link Juicer | Optimasi struktur tautan internal untuk SEO |
| **Analitik & Keamanan** | Jetpack | Monitoring performa, statistik traffic, dan keamanan dasar |

---

## Highlight Teknis Front-End

Bagian ini menjadi inti dari kontribusi teknis pada proyek, di mana penulis melakukan intervensi langsung terhadap lapisan presentasi (*presentation layer*) untuk mengatasi keterbatasan bawaan *page builder* dan mencapai standar visual tingkat enterprise.

### 1. Arsitektur Layout Direktori Dosen (CSS Grid & Flexbox)

Direktori dosen sebagai komponen dengan volume data terstruktur tertinggi pada situs — dibangun menggunakan kombinasi **CSS Grid** untuk kerangka tata letak dua dimensi (*macro-layout*) dan **Flexbox** untuk penyelarasan komponen kartu profil secara dinamis (*micro-layout*), menggantikan pendekatan *shortcode* bawaan yang kaku dan tidak fleksibel.

```css
/* Ilustrasi: Kerangka Grid Direktori Dosen */
.direktori-dosen-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 2rem;
}

.kartu-dosen {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
}
```

### 2. Responsive Design Tingkat Piksel (Media Queries)

Untuk menjamin konsistensi visual lintas perangkat (*desktop, tablet, mobile*), diterapkan strategi **Media Queries** dengan breakpoint kustom yang disesuaikan dengan kebutuhan spesifik komponen, bukan sekadar mengandalkan breakpoint generik dari tema.

```css
/* Ilustrasi: Breakpoint Kustom untuk Presisi Visual */
@media (max-width: 768px) {
  .direktori-dosen-grid {
    grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
    gap: 1rem;
  }
}

@media (max-width: 480px) {
  .kartu-dosen__nama {
    font-size: 0.875rem;
    line-height: 1.3;
  }
}
```

### 3. CSS Override & DOM Cleanup pada WPBakery

Salah satu tantangan teknis signifikan adalah menangani **elemen DOM kosong** (*empty `<div>` wrapper*) yang secara otomatis dihasilkan oleh WPBakery Page Builder, yang menyebabkan celah tata letak (*layout gap*) dan inkonsistensi tipografi. Penulis melakukan **override CSS** secara terarah untuk menetralisir elemen tersebut tanpa mengubah struktur inti *page builder*.

```css
/* Ilustrasi: Override untuk Membersihkan Wrapper Kosong WPBakery */
.wpb_wrapper:empty,
.vc_column-inner:empty {
  display: none !important;
}

.vc_row.vc_row-no-padding + .vc_row:empty {
  margin: 0 !important;
  padding: 0 !important;
}
```

> Hasil dari intervensi ini adalah tampilan yang **pixel-perfect**, bebas dari *whitespace* tidak diinginkan, serta tipografi yang tetap terjaga rapi di seluruh 60+ halaman situs.

---

## Peta Situs (Sitemap)

Struktur informasi disusun secara hierarkis untuk mengakomodasi kebutuhan navigasi berbagai segmen pengguna (calon mahasiswa, mahasiswa aktif, dan alumni):

```
📁 Root
│
├── 📁 Profil
│   ├── 📄 Program Magister (S2)
│   └── 📄 Program Doktor (S3)
│
├── 📁 Akademik
│   └── 📄 Kurikulum
│
├── 📁 Kemahasiswaan & Alumni
│   ├── 📄 Survei
│   └── 📄 Tracer Study
│
├── 📁 Admisi
│   └── 📄 Informasi Pendaftaran
│
└── 📁 Unduhan Dokumen
│    └── 📄 Repositori Formulir & Berkas Akademik
│
📁 Berita
│
│
📁 Tesimoni Alumni
```

---

## Peran & Tanggung Jawab

| Area Tanggung Jawab | Deskripsi |
|---|---|
| **Front-End Engineering** | Pengembangan dan kustomisasi CSS/JS untuk komponen kompleks (direktori dosen, layout responsif) |
| **UI/UX Refinement** | Perbaikan konsistensi visual dan pengalaman pengguna lintas 60+ halaman |
| **Bug Remediation** | Identifikasi dan perbaikan *DOM artifact* bawaan page builder |
| **SEO & Performance** | Konfigurasi Yoast SEO dan Internal Link Juicer untuk optimasi *search visibility* |
| **Maintenance** | Pengelolaan backup berkala (UpdraftPlus) dan monitoring (Jetpack) |

---

<div align="center">

**© Capstone - 28**

*Dokumen ini disusun untuk keperluan pengumpulan laporan dan tidak merepresentasikan basis kode produksi secara utuh.*

</div>
