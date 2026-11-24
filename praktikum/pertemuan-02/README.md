# Laporan Praktikum Workshop DevOps

## Pertemuan 2 — Konsep Container dan Instalasi Docker

| | |
|---|---|
| **Nama** | Tamisa Ulinda Marpaung |
| **NRP** | 3126640048 |
| **Mata Kuliah** | Workshop DevOps |
| **Program Studi** | D4 Lanjut Jenjang Teknik Informatika |
| **Institusi** | Politeknik Elektronika Negeri Surabaya |
| **Tahun** | 2026 |

📄 Versi PDF: [laporan.pdf](laporan.pdf)

---

## Daftar Isi

1. [Tujuan Pembelajaran](#1-tujuan-pembelajaran)
2. [Dasar Teori Singkat](#2-dasar-teori-singkat)
3. [Pelaksanaan Praktikum: Baseline Laboratorium](#3-pelaksanaan-praktikum-baseline-laboratorium)
4. [Jawaban Evaluasi dan Latihan Mandiri](#4-jawaban-evaluasi-dan-latihan-mandiri)
5. [Kesimpulan](#5-kesimpulan)

---

## 1. Tujuan Pembelajaran

- Memahami perbedaan mendasar antara model isolasi Virtual Machine (VM) dan Container.
- Menjalankan container pertama, memeriksa log aktivitas, dan masuk ke sistem operasi di dalam container secara interaktif.
- Membangun image aplikasi web custom secara mandiri dan deklaratif menggunakan Dockerfile.

## 2. Dasar Teori Singkat

*Containerization* adalah metode mengemas aplikasi beserta dependensinya agar dapat berjalan konsisten di berbagai lingkungan kerja. Berbeda dengan mesin virtual (VM) yang harus meniru seluruh perangkat keras dan memuat sistem operasi utuh (*guest OS*), container hanya memvirtualisasikan ruang lingkup proses dengan cara berbagi kernel dari OS utama (*host*). Docker memanfaatkan fitur kernel Linux seperti **namespace** untuk membatasi visibilitas proses dan **cgroup** untuk membatasi konsumsi sumber daya (CPU/RAM).

## 3. Pelaksanaan Praktikum: Baseline Laboratorium

### 3.1 Penyiapan Folder Kerja

![Langkah 3.1 — gambar 1](images/01.png)

### 3.2 Menjalankan Container Nginx & Akses Interaktif OS

![Langkah 3.2 — gambar 2](images/02.png)

![Langkah 3.2 — gambar 3](images/03.png)

![Langkah 3.2 — gambar 4](images/04.png)

### 3.3 Pembuatan Custom Web dengan Dockerfile

![Langkah 3.3 — gambar 5](images/05.png)

![Langkah 3.3 — gambar 6](images/06.png)

Jalankan container:

![Langkah 3.3 — gambar 7](images/07.png)

Cek apakah container sudah berjalan:

![Langkah 3.3 — gambar 8](images/08.png)

Pengujian akses web Nginx:

![Langkah 3.3 — gambar 9](images/09.png)

Pembuatan web:

![Langkah 3.3 — gambar 10](images/10.png)

![Langkah 3.3 — gambar 11](images/11.png)

Pembuatan file HTML:

![Langkah 3.3 — gambar 12](images/12.png)

![Langkah 3.3 — gambar 13](images/13.png)

![Langkah 3.3 — gambar 14](images/14.png)

![Langkah 3.3 — gambar 15](images/15.png)

![Langkah 3.3 — gambar 16](images/16.png)

![Langkah 3.3 — gambar 17](images/17.png)

Pembuatan custom web dan build Dockerfile:

![Langkah 3.3 — gambar 18](images/18.png)

![Langkah 3.3 — gambar 19](images/19.png)

![Langkah 3.3 — gambar 20](images/20.png)

![Langkah 3.3 — gambar 21](images/21.png)

## 4. Jawaban Evaluasi dan Latihan Mandiri

**1. Mengapa DevSecOps tidak dapat direduksi menjadi penambahan scanner pada pipeline?**

Karena DevSecOps adalah sistem sosio-teknis. Menambahkan scanner tanpa proses triase, batas toleransi risiko (*security gate*), dan kejelasan kepemilikan hanya akan menghasilkan antrean masalah dan peringatan yang diabaikan (*alert fatigue*). DevSecOps membutuhkan integrasi budaya, standar operasional, dan kolaborasi antar fungsi.

**2. Evidence apa yang membedakan klaim kontrol dari kontrol yang benar-benar terverifikasi?**

Klaim kontrol umumnya bersifat teoretis atau berbasis dokumentasi manual. Kontrol yang terverifikasi menghasilkan *evidence* (bukti) yang dapat dibaca oleh mesin dan diaudit, seperti laporan SARIF, JUnit XML, SBOM, *image signature*, dan log penyebaran yang mencakup identitas, waktu, versi alat, serta keputusan *waiver*.

**3. Bagaimana shared responsibility memengaruhi ownership risiko dan tindak lanjut temuan?**

*Shared responsibility* tidak berarti semua orang melakukan hal yang sama, melainkan mendistribusikan tanggung jawab sesuai konteks dan keahlian untuk mencegah area abu-abu. *Product owner* memegang *ownership* risiko, developer bertanggung jawab menerapkan perbaikan pada kode, *security* menyediakan model ancaman dan platform pengujian, serta *operations* mengelola deteksi lingkungan.

## 5. Kesimpulan

Implementasi DevSecOps menuntut lebih dari sekadar otomatisasi alat; ia membutuhkan penyelarasan sistem sosio-teknis yang mengutamakan umpan balik keamanan berkelanjutan. Perekaman *baseline* laboratorium di awal sangat penting untuk memastikan identifikasi risiko, eksekusi kontrol keamanan, dan pengumpulan bukti sistem yang konsisten untuk eksperimen selanjutnya.

---

⬅️ [Kembali ke daftar praktikum](../README.md)
