# Dokumentasi Workshop Day 1
**Building with AI, Managing Change with GitHub**

Pemateri: Nugi Farhan (Senior Product Designer)
Nama: Gabriel Maruli Malau | Kelompok 23 – Resident Evil 4

---

## 1. Rangkuman Materi

### A. Prompt Engineering
Prompt adalah instruksi atau masukan yang kita berikan kepada model AI untuk
mendapatkan hasil tertentu. Bentuknya bisa berupa pertanyaan sederhana, kata
kunci, instruksi yang rumit, atau potongan kode. Prompt engineering adalah cara
merancang instruksi agar AI memberikan jawaban yang tepat, relevan, dan layak
digunakan.

**Konteks adalah kunci.** Prompt singkat seperti "Create student task planner"
membuat AI harus menebak-nebak. Prompt dengan konteks yang jelas menghasilkan
output yang jauh lebih sesuai kebutuhan.

**Struktur prompt yang baik:**
- **Role**: peran yang diberikan ke AI (misalnya membantu membuat aplikasi
  untuk pemula).
- **Task**: tujuan atau tugas yang harus dikerjakan.
- **Context**: kebutuhan (requirements) dan batasan (constraints).
- **Format**: bentuk output yang diinginkan (misalnya kode lengkap per file,
  cara menjalankan, cara menguji).

**Taktik prompt yang efektif:**
- Gunakan kata kerja yang jelas untuk menentukan aksi.
- Tentukan panjang dan format output.
- Sebutkan target audiens.
- Sertakan fakta dan data yang relevan.
- Rujuk sumber atau dokumen tertentu.
- Definisikan istilah dan konsep penting.

**Keuntungan prompt engineering:**
1. Meningkatkan performa model AI.
2. Mengurangi bias dan respons yang offensive.
3. Meningkatkan kontrol dan predictability.
4. Memberikan pengalaman pengguna yang lebih baik.

### B. Git dan GitHub
**Git** adalah version control system yang melacak siapa, kapan, dan apa saja
yang diubah dalam suatu file. Git diciptakan oleh Linus Torvalds pada tahun
2005. Git bersifat terdistribusi (DVCS) dan bekerja secara lokal.

**GitHub** adalah platform berbasis web untuk menyimpan repository Git secara
online dan mendukung kolaborasi.

**Alur kerja Git (Git workflow):**
- **Working directory**: salinan satu versi proyek yang sedang dikerjakan di
  komputer.
- **Staging area (index)**: tempat menyimpan informasi perubahan apa saja yang
  akan masuk ke commit berikutnya.
- **Git directory (repository)**: tempat Git menyimpan metadata dan object
  database proyek. Bagian inilah yang disalin saat melakukan clone.

**Command penting:**

| Command | Fungsi |
|---|---|
| `git init` | Memulai repository baru |
| `git add .` | Memindahkan file ke staging area |
| `git commit -m "message"` | Menyimpan perubahan ke repository |
| `git remote add <name> <url>` | Menghubungkan repo lokal ke remote |
| `git push origin main` | Mengirim perubahan ke GitHub |
| `git pull origin main` | Mengambil dan menggabungkan perubahan dari GitHub |
| `git clone "url"` | Menyalin repository dari GitHub ke komputer |

**Setup yang dilakukan:**
1. Install Git dan cek dengan `git --version`.
2. Atur identitas dengan `git config --global user.name` dan `user.email`.
3. Install VS Code dan cek dengan `code --version`.
4. Membuat SSH key (`ssh-keygen -t ed25519`) dan menambahkannya ke GitHub, lalu
   verifikasi dengan `ssh -T git@github.com`.

### C. Praktik: Student Task Planner
Peserta membuat aplikasi sederhana "Student Task Planner" dengan bantuan AI,
lalu mengelola perubahannya dengan Git dan GitHub. Alurnya: install platform AI,
tulis prompt, `git init`, commit dan push ke GitHub, lakukan perubahan, lalu
commit dan push lagi.

---

## 2. Poin Penting dan Pengetahuan Baru
1. **Prompt yang spesifik menghasilkan hasil yang lebih baik.** Dengan struktur
   Role, Task, Context, dan Format, AI tidak perlu menebak maksud kita.
2. **Git dan GitHub itu berbeda.** Git adalah alat pelacak perubahan di komputer
   (lokal), sedangkan GitHub adalah tempat menyimpan repository Git secara
   online sekaligus media kolaborasi.
3. **Ada tiga area dalam Git.** Perubahan berpindah dari working directory ke
   staging area (`git add`), lalu ke repository (`git commit`).
4. **Commit bagaikan "save point"** yang mencatat perubahan, sehingga riwayat
   proyek bisa dilacak dan dikembalikan.
5. **Ada dua cara menghubungkan repo ke GitHub**: `git clone` untuk repo yang
   sudah ada, atau `git init` lalu `git remote add` untuk repo lokal.
6. **SSH key** adalah cara aman untuk autentikasi ke GitHub tanpa memasukkan
   password setiap kali. Alternatifnya adalah HTTPS dengan login lewat browser.
7. **Hasil dari AI tetap perlu diverifikasi.** Ini terlihat dari instruksi pada
   contoh prompt agar AI tidak mengklaim aplikasi berfungsi sebelum dicek.

---

## 3. Pendapat Pribadi tentang Day 1
Menurut saya, Day 1 workshop ini sangat bermanfaat karena menggabungkan dua
hal yang saling melengkapi: membuat sesuatu dengan bantuan AI dan mengelola
hasilnya dengan Git/GitHub. Sebelumnya saya mengira prompt hanya sekadar
bertanya ke AI, ternyata cara menyusunnya sangat berpengaruh pada hasil.

Bagian yang paling menarik bagi saya adalah struktur prompt (Role, Task,
Context, Format) dan konsep version control, karena langsung terasa
manfaatnya untuk proyek ke depan. Bagian yang cukup menantang adalah setup
awal, terutama koneksi ke GitHub. Saya sempat mengalami error saat clone
karena kesalahan penulisan URL dan SSH key yang belum terpasang, tetapi dari
situ saya belajar perbedaan antara SSH dan HTTPS serta cara membaca pesan
error.

Harapan saya untuk hari berikutnya adalah bisa lebih banyak praktik langsung,
misalnya bekerja dengan branch dan pull request, serta memakai AI untuk
mengembangkan proyek dengan lebih rapi.