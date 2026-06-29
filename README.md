# Capstone-28
# Website Pascasarjana Ilmu Komputer IPB University

![WordPress](https://img.shields.io/badge/Platform-WordPress-21759b?style=for-the-badge&logo=wordpress&logoColor=white)
![WPBakery](https://img.shields.io/badge/Page_Builder-WPBakery-eceff1?style=for-the-badge)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

---

##  Catatan Hak Akses & Konfidensialitas (Confidentiality Notice)
Pengembangan sistem informasi ini dilakukan secara langsung pada infrastruktur resmi milik institusi. Demi menjaga keamanan informasi, privasi data akademik, serta mematuhi kebijakan pembatasan akses server (*cPanel, Hosting, & Database*) yang dikelola oleh pihak IT Kampus, **source code inti WordPress, konfigurasi server, dan basis data (database) tidak dipublikasikan dalam repositori ini**. 

Repositori ini difungsikan sepenuhnya sebagai **dokumentasi arsitektur sistem, keputusan desain antarmuka (UI/UX), repositori aset visual, serta implementasi kustomisasi front-end** dari proyek yang telah diselesaikan.

---

## Deskripsi Proyek
Website Pascasarjana Ilmu Komputer IPB University merupakan platform digital resmi yang dirancang sebagai pusat informasi, media promosi, dan saluran publikasi bagi Program Magister (S2) dan Doktor (S3) Ilmu Komputer IPB University. 

Pengembangan website ini berfokus pada penyusunan struktur navigasi yang efisien, pengelolaan manajemen konten akademik, serta penyajian informasi yang transparan bagi mahasiswa aktif, dosen, maupun calon mahasiswa baru. Melalui optimalisasi fungsionalitas WordPress dan kustomisasi kode pada lapisan *front-end*, website ini mampu menghadirkan pengalaman pengguna yang informatif, responsif, dan selaras dengan identitas visual institusi.

---

## Fitur & Fungsionalitas Utama

### 1. Navigasi Terstruktur (Multi-level Dropdown)
* Sistem navigasi dirancang dengan arsitektur multi-level untuk memisahkan informasi secara spesifik. Terdapat pengelompokan yang jelas antara **Profil** dan **Akademik**, yang kemudian bercabang secara spesifik untuk **Program Magister** dan **Program Doktor**.
* Navigasi akademik mengakomodasi pemisahan jalur studi, seperti *Kurikulum by Course*, *Kurikulum by Research*, serta rincian *Deskripsi Mata Kuliah*.

### 2. Manajemen Direktori & Konten Akademik
* **Halaman Identitas Program:** Penyajian halaman Mandat, Visi, Misi, dan Tujuan yang menggunakan tipografi rapi dan konsisten dengan warna identitas institusi.
* **Direktori Dosen Interaktif:** Halaman daftar staf pengajar menggunakan *card layout* yang dilengkapi foto, gelar akademik, dan tombol aksi "Lihat Profil", serta terintegrasi dengan fitur pencarian teks (*Search*).
* **Tabel Kurikulum Terintegrasi:** Penyajian data akademik (Kode MK, Nama Mata Kuliah, SKS, Semester, dan Deskripsi) menggunakan struktur tabel berselang-seling warna (*striped table*) agar data berjumlah besar tetap mudah dibaca oleh mahasiswa.

### 3. Layanan Kemahasiswaan & Alumni
* **Survei Kepuasan & Evaluasi:** Fasilitas kuesioner terpusat yang dipisahkan antara evaluasi oleh mahasiswa aktif dan evaluasi retrospektif oleh alumni.
* **Portal Himpunan Alumni:** Halaman dedikasi yang memuat informasi kepengurusan dan struktur organisasi Himpunan Alumni Magister dan Doktor.
* **Studi Pelacakan (Tracer Study):** Sistem informasi dan publikasi terkait pelacakan jejak karier alumni sebagai bentuk pemenuhan Indikator Kinerja Utama (IKU) dan kebutuhan akreditasi institusi.

### 4. Aspek Teknis & Kustomisasi
* **Kustomisasi Tampilan Khusus:** Penyesuaian elemen antarmuka menggunakan kustomisasi kode HTML, CSS, dan JavaScript tanpa mengubah *core files* WordPress agar sistem tetap aman dan *upgradeable*.
* **Responsive Layout:** Dioptimalkan secara penuh untuk aksesibilitas lintas perangkat (Desktop, Tablet, dan Smartphone).

---

## Perancangan Antarmuka (UI/UX Aspect)
Proses perancangan dan implementasi antarmuka pada website ini didasarkan pada prinsip-prinsip berikut:

1. **Hierarki Informasi yang Jelas:** Menyusun tata letak konten berdasarkan prioritas kebutuhan pengguna (misal: kurikulum dan pendaftaran dibuat lebih mudah diakses).
2. **Identitas Visual Institusi:** Menggunakan palet warna resmi IPB University sebagai warna utama (*primary color*) untuk menjaga konsistensi brand dan kesan formal.
3. **Layout Berbasis Grid:** Penerapan struktur grid yang rapi, terutama pada halaman daftar dosen dan kartu (*card*) informasi, untuk meningkatkan keterbacaan (*readability*).
4. **Interaktivitas & Konsistensi UI:** Penyesuaian efek *hover*, desain tombol (*button*), struktur *header*, dan tipografi yang seragam di seluruh halaman guna menciptakan pengalaman navigasi yang intuitif.

---

## Tech Stack & Plugins

### Core Technologies
* **Platform:** WordPress (CMS)
* **Core Language:** PHP & MySQL
* **Front-end Customization:** HTML5, CSS3, JavaScript

### Tools & Plugins Terpasang
* **WPBakery Page Builder:** Digunakan untuk menyusun tata letak komponen visual dan struktur halaman secara dinamis.
* **Contact Form 7:** Implementasi formulir interaktif pada halaman kontak.
* **Yoast SEO:** Optimasi mesin pencari untuk memastikan artikel dan halaman akademik terindeks dengan baik.
* **LiteSpeed Cache:** Akselerasi kecepatan pemuatan halaman website (*web performance optimization*).
* **WP Mail SMTP:** Menjamin keandalan pengiriman email notifikasi sistem.

---

## 📂 Struktur Repositori
Untuk melengkapi transparansi proyek, repositori ini hanya memuat aset visual dan dokumentasi sebagai berikut:
```text
├── {Nama-File-Screenshot}.png/jpg    # Aset tangkapan layar antarmuka
└── README.md                         # Dokumentasi utama proyek
