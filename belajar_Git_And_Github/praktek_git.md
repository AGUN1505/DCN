**Panduan Instalasi Git & Konfigurasi GitHub**

- **Tujuan:** Panduan singkat untuk menginstal Git, mengonfigurasi identitas lokal, menyiapkan akses ke GitHub (SSH atau HTTPS), dan contoh alur kerja dasar.

**Prasyarat**:
- Sistem operasi: Windows, macOS, atau Linux.
- Akses internet untuk mengunduh installer dan menghubungkan ke GitHub.

**1. Instalasi Git**

- Windows:
	- Kunjungi https://git-scm.com/download/win dan unduh installer.
	- Jalankan installer dan terima pengaturan default kecuali Anda butuh konfigurasi khusus (biasanya pilihan default sudah baik: Git from the command line, Use OpenSSL, Checkout as-is).

- macOS:
	- Cara cepat: buka Terminal dan jalankan `git --version`. Jika belum terpasang, macOS akan menawarkan untuk menginstal Command Line Tools; ikuti instruksi.
	- Alternatif: install via Homebrew: `brew install git`.

- Linux (Debian/Ubuntu):
	- `sudo apt update && sudo apt install git -y`
	- Fedora: `sudo dnf install git`

**2. Verifikasi instalasi**

- Jalankan: `git --version`
- Anda akan melihat versi Git, mis. `git version 2.XX.X`.

**3. Konfigurasi Git lokal (wajib pertama kali)**

- Set nama dan email (digunakan pada commit):
	- `git config --global user.name "Nama Anda"`
	- `git config --global user.email "email@anda.com"`
- Periksa konfigurasi: `git config --list`
- Atur editor default (opsional): `git config --global core.editor "code --wait"` (untuk VS Code)

**4. Opsi autentikasi ke GitHub**

Pilihan utama: SSH (direkomendasikan) atau HTTPS (menggunakan Personal Access Token).

- SSH (lebih nyaman untuk push/pull tanpa memasukkan token berulang):
	1. Buat SSH key jika belum ada:
		 - `ssh-keygen -t ed25519 -C "email@anda.com"` (tekan Enter untuk lokasi default dan masukkan passphrase jika diinginkan)
		 - Jika sistem tidak mendukung ed25519, gunakan `ssh-keygen -t rsa -b 4096 -C "email@anda.com"`.
	2. Tambahkan SSH agent dan muat key:
		 - Windows (Git Bash / PowerShell): `eval "$(ssh-agent -s)"` lalu `ssh-add ~/.ssh/id_ed25519`
		 - macOS/Linux: `eval "$(ssh-agent -s)"` lalu `ssh-add ~/.ssh/id_ed25519`
	3. Salin isi public key dan tambahkan ke GitHub:
		 - Salin: `cat ~/.ssh/id_ed25519.pub` dan salin seluruh teks (atau buka file dengan editor).
		 - Di GitHub: Settings → SSH and GPG keys → New SSH key → tempelkan key → Save.
	4. Uji koneksi: `ssh -T git@github.com` (jawaban akan menyebutkan username Anda jika berhasil).

- HTTPS + Personal Access Token (PAT):
	1. Di GitHub, buka Settings → Developer settings → Personal access tokens → Tokens (classic) atau fine-grained tokens → Generate new token.
	2. Pilih scope yang diperlukan (repo untuk akses repo privat/public; workflow jika perlu).
	3. Salin token sekali lalu gunakan sebagai password ketika Git meminta kredensial pada HTTPS push/pull.
	4. Untuk menghindari memasukkan token berulang, aktifkan credential helper:
		 - Windows: `git config --global credential.helper manager-core`
		 - macOS: `git config --global credential.helper osxkeychain`
		 - Linux: `git config --global credential.helper cache` (atau gunakan libsecret untuk penyimpanan aman)

**5. Contoh alur kerja dasar**

- Clone repo (SSH): `git clone git@github.com:username/repo.git`
- Clone repo (HTTPS): `git clone https://github.com/username/repo.git`
- Buat branch baru: `git checkout -b fitur-baru`
- Tambah file dan commit:
	- `git add .`
	- `git commit -m "Pesan commit yang jelas"`
- Push branch ke origin: `git push -u origin fitur-baru`

**6. Tips verifikasi cepat**

- Cek konfigurasi global: `git config --global --list`
- Cek apakah SSH terhubung: `ssh -T git@github.com`
- Cek remote repo: `git remote -v`

**7. Troubleshooting singkat**

- Jika Git tidak ditemukan setelah instalasi di Windows: pastikan opsi "Git from the command line" dipilih pada installer, atau restart terminal.
- Jika push via SSH gagal: periksa `~/.ssh/authorized_keys` (server-side), pastikan public key sudah ditambahkan, dan jalankan `ssh -vT git@github.com` untuk debug.
- Jika credential helper meminta token berulang: hapus cache credential dan lakukan login ulang atau konfigurasikan credential helper sesuai OS.

**8. Referensi singkat**
- Dokumentasi Git: https://git-scm.com/doc
- Dokumentasi GitHub (SSH): https://docs.github.com/en/authentication/connecting-to-github-with-ssh
- Dokumentasi GitHub (PAT): https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token

**done**
**donee**
