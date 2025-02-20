---
title: Instalasi Lingkungan Python
layout: default
permalink: /course/env-install
published: true
---

**Table of Contents**
1. [Panduan Instalasi Anaconda](#panduan-instalasi-anaconda)
2. [Instalasi VSCODE dan Extension](#instalasi-vscode-dan-extension)
3. [Mendaftar Github Student Developer Pack](#github-student-developer-pack)
4. [Tutorial Git](#tutorial-git-dasar)
5. [NEW...!!! UV Python Environment](#uv-python-environment)

# Panduan Instalasi Anaconda

Berikut adalah panduan untuk menginstal Anaconda atau Miniconda di Windows dan MacOS

> Anaconda dan Miniconda adalah dua distribusi yang berbeda untuk mengelola lingkungan Python, masing-masing dengan kelebihan dan tujuan penggunaannya sendiri. Anaconda adalah distribusi yang lengkap dan komprehensif, menyediakan Python serta lebih dari 1.500 paket yang digunakan dalam data science, seperti Jupyter Notebook, Spyder, NumPy, SciPy, Pandas, dan Matplotlib. Ukurannya yang besar, biasanya lebih dari 500 MB. Sebaliknya, Miniconda adalah versi minimalis dari Anaconda, hanya mencakup conda, Python, dan beberapa paket dasar, dengan ukuran installer yang sangat kecil, kurang dari 50 MB.

## Menginstal Anaconda/Miniconda di Windows

1. **Unduh Installer:**
   - Kunjungi [situs resmi Anaconda](https://www.anaconda.com/products/distribution#download-section) atau [situs resmi Miniconda](https://docs.conda.io/en/latest/miniconda.html).
   - Pilih installer yang sesuai dengan sistem operasi Windows Anda (64-bit atau 32-bit).

2. **Jalankan Installer:**
   - Klik dua kali file installer yang sudah diunduh.
   - Ikuti petunjuk pada layar, pilih "Install for me only" kecuali jika Anda ingin Anaconda/Miniconda tersedia untuk semua pengguna komputer.

3. **Pilih Lokasi Instalasi:**
   - Pilih lokasi di mana Anda ingin menginstal Anaconda/Miniconda. Disarankan untuk menggunakan lokasi default.

4. **Konfigurasi PATH:**
   - Pada langkah ini, Anda akan melihat opsi untuk menambahkan Anaconda/Miniconda ke PATH environment variable. Sangat disarankan untuk tidak mencentang kotak ini agar tidak terjadi konflik dengan software lain. Namun, pastikan Anda mencentang opsi untuk mengatur Anaconda/Miniconda sebagai Python default Anda.

5. **Selesaikan Instalasi:**
   - Klik "Install" dan tunggu hingga proses instalasi selesai.
   - Setelah instalasi selesai, Anda dapat memverifikasi instalasi dengan membuka Anaconda Prompt (untuk Anaconda) atau Command Prompt (untuk Miniconda) dan menjalankan perintah `conda --version`.

## Menginstal Anaconda/Miniconda di MacOS

1. **Unduh Installer:**
   - Kunjungi [situs resmi Anaconda](https://www.anaconda.com/products/distribution#download-section) atau [situs resmi Miniconda](https://docs.conda.io/en/latest/miniconda.html).
   - Pilih installer yang sesuai dengan sistem operasi macOS Anda (Intel atau Apple M1/M2 Chip).

2. **Jalankan Installer:**
   - Buka terminal dan navigasikan ke folder tempat file installer diunduh. Misalnya, jika file diunduh di folder `Downloads`, ketik:
     ```
     cd ~/Downloads
     ```
   - Ubah izin file installer agar dapat dieksekusi dengan perintah:
     ```
     chmod +x nama_file_installer.sh
     ```
   - Jalankan installer dengan perintah:
     ```
     ./nama_file_installer.sh
     ```

3. **Ikuti Instruksi di Terminal:**
   - Ikuti petunjuk pada layar untuk menyetujui lisensi dan memilih lokasi instalasi.
   - Disarankan untuk menggunakan lokasi default (biasanya di `~/anaconda3` atau `~/miniconda3`).

4. **Konfigurasi PATH:**
   - Setelah instalasi selesai, installer akan menanyakan apakah Anda ingin menambahkan Anaconda/Miniconda ke PATH environment variable. Ketik `yes` dan tekan Enter.

5. **Selesaikan Instalasi:**
   - Tutup terminal dan buka kembali untuk memuat perubahan PATH.
   - Verifikasi instalasi dengan menjalankan perintah `conda --version` di terminal.

Berikut adalah panduan untuk menginstal Anaconda atau Miniconda di Ubuntu/Linux:

## Menginstal Anaconda/Miniconda di Ubuntu/Linux

1. **Unduh Installer:**
   - Kunjungi [situs resmi Anaconda](https://www.anaconda.com/products/distribution#download-section) atau [situs resmi Miniconda](https://docs.conda.io/en/latest/miniconda.html).
   - Unduh installer yang sesuai untuk Linux. Biasanya, file installer akan memiliki ekstensi `.sh`.

2. **Buka Terminal:**
   - Buka terminal di sistem Ubuntu/Linux Anda.

3. **Navigasi ke Folder Unduhan:**
   - Pindah ke direktori tempat file installer diunduh. Misalnya, jika file diunduh ke folder `Downloads`, ketik:
     ```bash
     cd ~/Downloads
     ```

4. **Ubah Izin File Installer:**
   - Ubah izin file installer agar dapat dieksekusi dengan perintah:
     ```bash
     chmod +x nama_file_installer.sh
     ```

5. **Jalankan Installer:**
   - Jalankan installer dengan perintah:
     ```bash
     ./nama_file_installer.sh
     ```
   - Gantilah `nama_file_installer.sh` dengan nama file installer yang sebenarnya.

6. **Ikuti Instruksi di Terminal:**
   - Ikuti petunjuk yang muncul di terminal untuk menyetujui lisensi dan memilih lokasi instalasi.
   - Disarankan untuk menggunakan lokasi default (biasanya di `~/anaconda3` atau `~/miniconda3`).

7. **Konfigurasi PATH:**
   - Setelah instalasi selesai, installer akan menanyakan apakah Anda ingin menambahkan Anaconda/Miniconda ke PATH environment variable. Ketik `yes` dan tekan Enter.
   - Jika installer tidak menambahkan PATH secara otomatis, Anda bisa menambahkannya secara manual dengan menambahkan baris berikut di akhir file `~/.bashrc`:
     ```bash
     export PATH="~/anaconda3/bin:$PATH"
     ```
     atau
     ```bash
     export PATH="~/miniconda3/bin:$PATH"
     ```
   - Setelah menambahkan baris di atas, muat ulang file `~/.bashrc` dengan perintah:
     ```bash
     source ~/.bashrc
     ```

8. **Verifikasi Instalasi:**
   - Verifikasi instalasi dengan menjalankan perintah berikut di terminal:
     ```bash
     conda --version
     ```

## Panduan Video

Video di bawah ini menggunakan bahasa Indonesia. Kredit: Pacman AI
1. [Untuk Windows](https://www.youtube.com/watch?v=XyudQ3B3OWI)
2. [Untuk MacOS](https://youtu.be/rhc-F-BVo1Y?si=K51clwd1Kfzq9qDa)
3. [Untuk Ubuntu](https://youtu.be/PHkCmuzgHOo?si=y-UuOKnwzJG-by7s)

# Instalasi VSCode dan Extension

### VSCode
Silahkan download dari [tautan berikut](https://code.visualstudio.com/download)

### Extension yang diperlukan
1. [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
2. [Jupyter](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter)
3. [Github Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot)

# Github Student Developer Pack

Berikut adalah langkah-langkah untuk mendaftar GitHub Student Developer Pack:

1. **Buat Akun GitHub:**
   - Jika Anda belum memiliki akun GitHub, kunjungi [github.com](https://github.com) dan klik "Sign up" untuk membuat akun baru.
   - Ikuti langkah-langkah untuk menyelesaikan proses pendaftaran dan verifikasi email Anda.

2. **Masuk ke GitHub Education:**
   - Kunjungi halaman [GitHub Education](https://education.github.com/pack).
   - Klik tombol "Get your pack" untuk memulai proses pendaftaran.

3. **Verifikasi Status Pelajar:**
   - Anda akan diminta untuk masuk ke akun GitHub Anda jika belum masuk.
   - Isi formulir pendaftaran dengan informasi yang diminta, seperti nama lengkap, nama institusi pendidikan, dan alamat email institusi pendidikan Anda.
   - Untuk memverifikasi status pelajar, Anda dapat menggunakan salah satu dari dua cara berikut:
     - Mengunggah foto atau scan kartu identitas pelajar yang valid.
     - Menggunakan alamat email institusi pendidikan (misalnya, email dengan domain .edu atau domain khusus institusi pendidikan lainnya).

4. **Lengkapi Informasi Tambahan:**
   - Terkadang, GitHub mungkin meminta informasi tambahan untuk memverifikasi status pelajar Anda, seperti URL ke profil institusi pendidikan atau dokumen pendukung lainnya.

5. **Tunggu Persetujuan:**
   - Setelah mengirimkan aplikasi, Anda akan menerima email konfirmasi bahwa permohonan Anda sedang diproses.
   - Proses verifikasi biasanya memerlukan waktu beberapa hari hingga satu minggu.

6. **Akses GitHub Student Developer Pack:**
   - Setelah permohonan Anda disetujui, Anda akan menerima email pemberitahuan.
   - Anda sekarang dapat mengakses GitHub Student Developer Pack yang berisi berbagai manfaat dan penawaran dari berbagai mitra, seperti domain gratis, layanan cloud, alat pengembangan, dan banyak lagi.

Dengan mengikuti langkah-langkah di atas, Anda dapat mendaftar dan memanfaatkan berbagai manfaat yang ditawarkan oleh GitHub Student Developer Pack untuk mendukung kegiatan belajar dan proyek pengembangan Anda.

### Panduan Video

[How to Apply for GitHub Students benefits (GitHub Student Developer Pack)](https://www.youtube.com/watch?v=iyThW3RvZpk)

# Tutorial Git Dasar

Berikut adalah tutorial dasar tentang penggunaan Git dengan GitHub:

### 1. Persiapan Awal
#### Menginstal Git
- **Windows:** Unduh Git dari [situs resmi Git](https://git-scm.com/downloads) dan jalankan installer.
- **MacOS:** Buka terminal dan ketik `git`, jika belum terinstal, Anda akan diberikan pilihan untuk menginstalnya.
- **Linux:** Instal Git menggunakan package manager, misalnya untuk Ubuntu:
  ```bash
  sudo apt-get update
  sudo apt-get install git
  ```

#### Mengkonfigurasi Git
Setelah menginstal Git, konfigurasikan informasi pengguna:
```bash
git config --global user.name "Nama Anda"
git config --global user.email "email@example.com"
```

### 2. Membuat Repository Baru
#### Menggunakan GitHub
1. **Buat Repository Baru:**
   - Kunjungi [GitHub](https://github.com) dan masuk ke akun Anda.
   - Klik tombol "New" atau ikon "+" di sudut kanan atas dan pilih "New repository".
   - Isi nama repository dan deskripsi (opsional), pilih publik atau privat, dan klik "Create repository".

#### Menggunakan Git
1. **Buat Folder Lokal:**
   ```bash
   mkdir nama-repo
   cd nama-repo
   ```
2. **Inisialisasi Repository Git:**
   ```bash
   git init
   ```

### 3. Menambahkan Remote Repository
Hubungkan repository lokal Anda dengan repository GitHub:
```bash
git remote add origin https://github.com/username/nama-repo.git
```

### 4. Menambahkan dan Meng-commit Perubahan
1. **Buat atau Tambahkan File:**
   - Buat file baru, misalnya `README.md`, dan tambahkan beberapa konten.
2. **Tambahkan File ke Staging Area:**
   ```bash
   git add README.md
   ```
3. **Commit Perubahan:**
   ```bash
   git commit -m "Menambahkan README"
   ```

### 5. Mengirim Perubahan ke GitHub
1. **Push ke Repository GitHub:**
   ```bash
   git push origin master
   ```

### 6. Melakukan Perubahan dan Melacak Versi
1. **Lakukan Perubahan pada File:**
   - Edit file yang ada atau tambahkan file baru.
2. **Tambahkan dan Commit Perubahan:**
   ```bash
   git add .
   git commit -m "Deskripsi perubahan"
   ```
3. **Push Perubahan:**
   ```bash
   git push origin master
   ```

### 7. Mengelola Branch
Branch memungkinkan Anda untuk bekerja pada fitur atau perbaikan secara terpisah dari branch utama (master/main).

1. **Buat Branch Baru:**
   ```bash
   git checkout -b nama-branch
   ```
2. **Pindah ke Branch:**
   ```bash
   git checkout nama-branch
   ```
3. **Push Branch ke GitHub:**
   ```bash
   git push origin nama-branch
   ```

### 8. Menggabungkan Branch
Setelah selesai bekerja pada branch, gabungkan perubahan ke branch utama.

1. **Pindah ke Branch Utama:**
   ```bash
   git checkout master
   ```
2. **Gabungkan Branch:**
   ```bash
   git merge nama-branch
   ```
3. **Push Perubahan:**
   ```bash
   git push origin master
   ```

### 9. Menarik Perubahan dari GitHub
Untuk memperbarui repository lokal Anda dengan perubahan terbaru dari GitHub:

1. **Pull Perubahan:**
   ```bash
   git pull origin master
   ```

Dengan mengikuti langkah-langkah ini, Anda dapat memulai penggunaan Git dan GitHub untuk mengelola proyek Anda dengan versi kontrol yang efisien.

# UV Python Environment

> Diterjemahkan dari postingan Sebastian Raschka pada [tautan berikut ini](https://github.com/rasbt/LLMs-from-scratch/blob/main/setup/01_optional-python-setup-preferences/README.md)

Saya telah lama menggunakan Conda dan pip, namun baru-baru ini, package uv telah mendapatkan popularitas yang signifikan karena menyediakan cara yang lebih cepat dan efisien untuk menginstal package dan menyelesaikan dependencies.

Saya merekomendasikan untuk memulai dengan Option 1: Menggunakan uv karena ini adalah pendekatan yang lebih modern di tahun 2025. Jika Anda mengalami masalah dengan Option 1, pertimbangkan Option 2: Menggunakan Conda.

## Step 1: Instalasi Python
Jika Anda belum pernah menginstal Python secara manual di sistem Anda sebelumnya, sangat disarankan untuk melakukannya. Ini membantu mencegah potensi konflik dengan instalasi Python bawaan sistem operasi Anda, yang dapat menyebabkan masalah.

Namun, bahkan jika Anda sudah menginstal Python di sistem Anda sebelumnya, periksa apakah Anda memiliki versi Python modern yang terinstal (disarankan 3.10 atau yang lebih baru) dengan menjalankan kode berikut di terminal:

```bash
python --version
```

Jika menampilkan versi 3.10 atau yang lebih baru, tidak diperlukan tindakan lebih lanjut.

### Instalasi Python Secara Manual

#### Untuk Linux/Ubuntu:
```bash
sudo apt update
sudo apt install python3
```

#### Untuk macOS:
1. Unduh installer dari [python.org](https://www.python.org/downloads/)
2. Buka file .pkg yang diunduh
3. Ikuti petunjuk installer
4. Verifikasi instalasi:
```bash
python3 --version
```

#### Untuk Windows:
1. Kunjungi [python.org](https://www.python.org/downloads/)
2. Unduh installer Windows terbaru
3. Jalankan installer
4. **PENTING:** Centang "Add Python to PATH"
5. Pilih "Install Now"
6. Verifikasi di Command Prompt:
```cmd
python --version
```

## Step 2: Instalasi UV

Sangat disarankan untuk menginstal paket Python dalam virtual environment terpisah untuk menghindari modifikasi paket sistem yang mungkin dibutuhkan oleh sistem operasi Anda. Untuk membuat virtual environment di folder saat ini, ikuti tiga langkah di bawah ini.

1. Instal uv
```bash
pip install uv
```

2. Buat virtual environment
```bash
uv venv --python=python3.10
```

3. Aktifkan virtual environment
```bash
source .venv/bin/activate
```

**Catatan**

Jika Anda menggunakan Windows, Anda mungkin perlu mengganti perintah di atas dengan `source .venv/Scripts/activate` atau `.venv/Scripts/activate`.

Perlu diingat bahwa Anda harus mengaktifkan virtual environment setiap kali memulai sesi terminal baru. Misalnya, jika Anda me-restart terminal atau komputer dan ingin melanjutkan pekerjaan pada proyek keesokan harinya, cukup jalankan `source .venv/bin/activate` di folder proyek untuk mengaktifkan kembali virtual environment Anda.

## Step 3: Instalasi Library Python

Setelah mengaktifkan virtual environment Anda, Anda dapat menginstal paket Python menggunakan uv. Contohnya:

```bash
uv pip install packaging
```

Untuk menginstal semua paket yang diperlukan dari file requirements.txt (seperti yang ada di level teratas repositori GitHub ini), jalankan perintah berikut, dengan asumsi file berada di direktori yang sama dengan sesi terminal Anda:

```bash
uv pip install -U -r requirements.txt
```

Atau, instal dependencies terbaru langsung dari repositori:

```bash
uv pip install -U -r https://raw.githubusercontent.com/rasbt/LLMs-from-scratch/refs/heads/main/requirements.txt
```