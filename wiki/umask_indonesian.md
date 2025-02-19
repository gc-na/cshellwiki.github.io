# [Sistem Operasi] C Shell (csh) umask: Mengatur izin file default

## Overview
Perintah `umask` digunakan untuk mengatur izin default yang diterapkan pada file dan direktori baru yang dibuat oleh pengguna. Dengan menggunakan `umask`, Anda dapat menentukan izin akses yang akan dibatasi untuk file dan direktori yang baru dibuat.

## Usage
Berikut adalah sintaks dasar dari perintah `umask`:

```csh
umask [options] [arguments]
```

## Common Options
- `-S` : Menampilkan umask dalam format simbolik.
- `-p` : Menampilkan nilai umask saat ini.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `umask`:

1. **Menampilkan nilai umask saat ini:**
   ```csh
   umask
   ```

2. **Menampilkan nilai umask dalam format simbolik:**
   ```csh
   umask -S
   ```

3. **Mengatur umask untuk membatasi izin file baru:**
   ```csh
   umask 027
   ```
   Dalam contoh ini, file baru akan memiliki izin 640 (rw-r-----).

4. **Mengatur umask untuk membatasi izin direktori baru:**
   ```csh
   umask 007
   ```
   Ini akan memberikan izin 770 (rwxrwx---) untuk direktori baru.

## Tips
- Selalu periksa nilai umask Anda sebelum membuat file atau direktori baru untuk memastikan izin yang sesuai.
- Gunakan umask yang lebih ketat di lingkungan yang sensitif untuk meningkatkan keamanan.
- Anda dapat menambahkan perintah `umask` ke dalam file konfigurasi shell Anda (seperti `.cshrc`) untuk menetapkan nilai umask default setiap kali Anda membuka sesi shell baru.