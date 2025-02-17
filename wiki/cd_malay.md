# [Linux] Bash cd Penggunaan: Menukar direktori kerja semasa

## Overview
Perintah `cd` (change directory) digunakan dalam Bash untuk menukar direktori kerja semasa. Dengan menggunakan perintah ini, pengguna boleh bergerak ke lokasi lain dalam sistem fail.

## Usage
Sintaks asas untuk perintah `cd` adalah seperti berikut:
```
cd [options] [arguments]
```

## Common Options
- `..` : Menukar ke direktori induk (parent directory).
- `-` : Menukar ke direktori sebelumnya.
- `~` : Menukar ke direktori home pengguna semasa.

## Common Examples
1. Menukar ke direktori induk:
   ```bash
   cd ..
   ```

2. Menukar ke direktori tertentu:
   ```bash
   cd /path/to/directory
   ```

3. Menukar ke direktori sebelumnya:
   ```bash
   cd -
   ```

4. Menukar ke direktori home:
   ```bash
   cd ~
   ```

5. Menukar ke direktori yang baru dibuka:
   ```bash
   cd /var/log
   ```

## Tips
- Gunakan `cd -` untuk cepat kembali ke direktori sebelumnya.
- Anda boleh menggunakan `cd` tanpa sebarang argumen untuk kembali ke direktori home anda.
- Untuk memudahkan navigasi, ingatlah untuk menggunakan tab untuk melengkapkan nama direktori secara automatik.