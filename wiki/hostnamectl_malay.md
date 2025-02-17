# [Linux] Bash hostnamectl Penggunaan: Mengurus nama hos sistem

## Overview
Perintah `hostnamectl` digunakan untuk mengurus dan menampilkan maklumat tentang nama hos sistem Linux. Ia membolehkan pengguna untuk menetapkan nama hos, nama statik, dan nama dinamik, serta mendapatkan maklumat tentang sistem.

## Usage
Sintaks asas untuk perintah `hostnamectl` adalah seperti berikut:

```bash
hostnamectl [options] [arguments]
```

## Common Options
- `set-hostname`: Menetapkan nama hos baru.
- `status`: Menampilkan maklumat tentang nama hos semasa dan status sistem.
- `set-icon-name`: Menetapkan nama ikon untuk sistem.
- `set-chassis`: Menetapkan jenis chasis sistem (contohnya, desktop, laptop).
- `help`: Menampilkan maklumat bantuan tentang perintah ini.

## Common Examples
1. **Menampilkan maklumat nama hos semasa:**
   ```bash
   hostnamectl status
   ```

2. **Menetapkan nama hos baru:**
   ```bash
   sudo hostnamectl set-hostname nama-baru
   ```

3. **Menetapkan nama ikon untuk sistem:**
   ```bash
   sudo hostnamectl set-icon-name nama-ikon
   ```

4. **Menetapkan jenis chasis sistem:**
   ```bash
   sudo hostnamectl set-chassis laptop
   ```

## Tips
- Sentiasa gunakan `sudo` apabila menetapkan nama hos atau melakukan perubahan lain yang memerlukan hak akses pentadbir.
- Pastikan nama hos yang anda pilih tidak mengandungi ruang atau karakter khas.
- Selepas mengubah nama hos, anda mungkin perlu log keluar dan masuk semula untuk melihat perubahan tersebut berkuatkuasa.