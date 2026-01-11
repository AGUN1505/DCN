# Git dan GitHub

Pada materi **Git dan GitHub**, kita telah mempelajari sejarah, konsep dasar, hingga praktik penggunaan Git dan GitHub dalam pengembangan perangkat lunak secara kolaboratif. Berikut adalah rangkuman dari seluruh materi tersebut.

---

## Pengantar Git

Git dikembangkan pada tahun **2005** oleh **Linus Torvalds** bersama timnya. Git dibuat untuk mendukung:

* Kolaborasi antar tim
* Pengelolaan versi proyek
* Kontrol perubahan kode secara terstruktur

Kolaborasi dapat dilakukan dengan:

* Membuat proyek **open source**
* Mengatur akses kolaborator secara privat

---

## Istilah dan Perintah Dasar Git

Berikut beberapa istilah dan perintah penting dalam Git:

| Perintah       | Fungsi                                                          |
| -------------- | --------------------------------------------------------------- |
| Git Repository | Media penyimpanan file proyek di server Git                     |
| Git Branch     | Percabangan untuk versi atau fitur baru                         |
| Git Fork       | Menyalin repository orang/organisasi lain ke repository pribadi |
| Git Clone      | Mengambil repository dan menyimpannya secara lokal              |
| Git Commit     | Snapshot perubahan repository                                   |
| Git Push       | Mengirim perubahan ke repository server                         |
| Git Pull       | Mengambil perubahan dari repository server                      |

---

## GitHub

**GitHub** adalah platform hosting repository Git berbasis cloud yang sangat populer dan mudah digunakan. GitHub mempermudah kolaborasi tim dalam pengembangan proyek.

### Menu Utama GitHub

* **Explore Repository**
* **Sign Up**
* **Sign In**

### Fitur Pendukung GitHub

* **New Repository** – Membuat repository baru (public/private)
* **Import Repository** – Mengimpor proyek dari platform lain
* **Gist** – Berbagi potongan kode atau catatan
* **GitHub Organization** – Kolaborasi dalam skala organisasi
* **GitHub Project** – Manajemen tugas dan alur kerja proyek

---

## Latihan GitHub

### 1. Membuat Akun GitHub

Langkah-langkah:

1. Akses `https://github.com/signup`
2. Isi data pendaftaran
3. Verifikasi email
4. (Opsional) Tambahkan email cadangan

---

### 2. Mengeksplorasi Proyek GitHub

Langkah-langkah:

* Cari repository menggunakan fitur **Search**
* Analisis jumlah **watch**, **star**, dan **fork**
* Memberikan **star**
* Melihat **contributor** dan **collaborator**

---

### 3. Mengenal GitHub Dashboard

Dashboard menampilkan:

* Aktivitas repository
* Pull Request
* Issues
* Marketplace
* Explore
* Settings

---

## Kolaborator dan Kontributor

* **Kolaborator**: Memiliki akses langsung ke repository
* **Kontributor**: Memberikan kontribusi melalui pull request

### Level Akses Kolaborator (Organisasi)

1. **Read**
2. **Triage**
3. **Write**
4. **Maintain**
5. **Admin**

---

## Sistem Notifikasi GitHub

Notifikasi akan diterima ketika:

* Mengikuti repository (watch)
* Terlibat dalam PR atau issues
* Mendapat mention (`@username`)
* Menjadi anggota tim

Notifikasi dapat dikelola melalui **Inbox Notifications** dan **Settings Notifications**.

---

# Dasar Git

Git mempermudah:

* Pelacakan perubahan file
* Manajemen versi proyek

### Jenis Repository

* **Local Repository**
* **Remote Repository** (GitHub, GitLab, Bitbucket)

---

## Visibilitas Repository

* **Private**: Akses terbatas
* **Public**: Terbuka untuk umum

---

## Inisialisasi Repository

* Add README
* Add `.gitignore`
* Choose License

---

## Perintah Git Penting

| Perintah     | Fungsi                                        |
| ------------ | --------------------------------------------- |
| Git Commit   | Menyimpan perubahan                           |
| Git Checkout | Berpindah commit atau branch                  |
| Git Reset    | Mengembalikan commit dan menghapus history    |
| Git Revert   | Membatalkan perubahan tanpa menghapus history |

---

## README dan Markdown

README biasanya ditulis menggunakan **Markdown (.md)**.

| Format     | Simbol |
| ---------- | ------ |
| Heading    | `#`    |
| Subheading | `--`   |
| Italic     | `*`    |
| List       | `-`    |

---

## Release dan Versioning

Contoh penulisan tag versi:

* `v1.0`
* `v1.0.0`
* `v3.1-alpha`
* `v4.2-beta`

---

# Git Branch

Branch digunakan untuk:

* Mengembangkan fitur baru
* Bug fixing
* Kolaborasi tim

### Operasi Branch

* `git checkout`
* `git merge`
* Pull Request

### Conflict

Conflict terjadi saat dua branch mengubah baris yang sama. Conflict harus diselesaikan secara manual sebelum merge.

---

# Kolaborasi dengan Tim

### Cara Kolaborasi

* Repository Organisasi
* Repository Pribadi

### Fork & Pull Request

* Fork → Salin repository
* Commit perubahan
* Pull Request → Minta perubahan digabung

---

## Squash & Merge

Digunakan untuk:

* Merapikan riwayat commit
* Menggabungkan beberapa commit kecil menjadi satu

---

## Network Graph

Digunakan untuk melihat alur commit dan PR dalam repository.

---

## Code Review

Tujuan:

* Menjaga kualitas kode
* Menghindari bug

### Status Review:

* **Comment**
* **Approve**
* **Request Changes**

---

# Studi Kasus Kolaborasi

Jika memiliki akses:

* Buat branch
* Commit
* Pull Request

Jika tidak memiliki akses:

* Fork repository
* Commit
* Pull Request
* Code Review
* Approve & Merge

---

# GitHub sebagai Portofolio

**Portofolio ≠ CV**

* CV → Klaim kemampuan
* Portofolio → Bukti nyata

### Alasan GitHub Cocok untuk Portofolio

* Mudah dirancang (Markdown)
* Portabel
* Mendukung kolaborasi
* Biaya rendah
* Riwayat perubahan tercatat

Repository dengan nama akun GitHub akan otomatis tampil di halaman profil.

---


