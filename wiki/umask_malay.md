# [Linux] Bash umask Penggunaan: Mengawal hak akses fail

## Overview
Perintah `umask` digunakan untuk menetapkan nilai umask yang menentukan hak akses lalai untuk fail dan direktori yang baru dibuat. Nilai umask ini mengawal siapa yang boleh membaca, menulis, atau melaksanakan fail yang dicipta oleh pengguna.

## Usage
Sintaks asas untuk perintah `umask` adalah seperti berikut:

```bash
umask [options] [arguments]
```

## Common Options
- `-S`: Menunjukkan nilai umask dalam format simbolik.
- `-p`: Menunjukkan nilai umask semasa untuk shell yang sedang berjalan.

## Common Examples
Berikut adalah beberapa contoh praktikal menggunakan perintah `umask`:

1. **Menunjukkan nilai umask semasa:**
   ```bash
   umask
   ```

2. **Menetapkan nilai umask kepada 027:**
   ```bash
   umask 027
   ```

3. **Menunjukkan nilai umask dalam format simbolik:**
   ```bash
   umask -S
   ```

4. **Menetapkan nilai umask kepada 007:**
   ```bash
   umask 007
   ```

## Tips
- Sentiasa semak nilai umask semasa sebelum mencipta fail untuk memastikan hak akses yang betul.
- Gunakan nilai umask yang lebih ketat untuk fail sensitif bagi meningkatkan keselamatan.
- Ingat bahawa nilai umask adalah spesifik kepada sesi shell; ia tidak akan kekal selepas sesi ditutup kecuali ditetapkan dalam fail konfigurasi seperti `.bashrc`.