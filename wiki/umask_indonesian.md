# [Linux] Bash umask Penggunaan: Mengatur izin file default

## Overview
Perintah `umask` digunakan untuk mengatur izin file default yang diberikan kepada file dan direktori baru yang dibuat oleh pengguna. Dengan menggunakan `umask`, Anda dapat menentukan izin yang tidak akan diterapkan pada file dan direktori baru.

## Usage
Berikut adalah sintaks dasar dari perintah `umask`:

```bash
umask [options] [arguments]
```

## Common Options
- `-S`: Menampilkan umask dalam format simbolik.
- `-p`: Menampilkan umask saat ini dalam format simbolik.
- `N`: Mengatur umask ke nilai numerik yang ditentukan.

## Common Examples
Berikut adalah beberapa contoh praktis penggunaan perintah `umask`:

1. **Menampilkan umask saat ini:**
   ```bash
   umask
   ```

2. **Menampilkan umask dalam format simbolik:**
   ```bash
   umask -S
   ```

3. **Mengatur umask ke nilai numerik 027:**
   ```bash
   umask 027
   ```

4. **Mengatur umask ke nilai simbolik:**
   ```bash
   umask u=rwx,g=rx,o=
   ```

5. **Mengatur umask sementara untuk sesi terminal saat ini:**
   ```bash
   umask 002
   # Buat file baru dan periksa izin
   touch file_baru.txt
   ls -l file_baru.txt
   ```

## Tips
- Selalu periksa umask Anda sebelum membuat file baru untuk memastikan izin yang tepat.
- Gunakan umask yang lebih ketat di lingkungan produksi untuk meningkatkan keamanan.
- Anda dapat menambahkan perintah `umask` ke file konfigurasi shell Anda (seperti `.bashrc` atau `.bash_profile`) untuk mengatur umask secara otomatis saat login.