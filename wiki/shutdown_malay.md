# [Linux] Bash shutdown penggunaan: Mematikan sistem

## Overview
Perintah `shutdown` digunakan untuk mematikan atau merestart sistem Linux dengan cara yang teratur. Ia membolehkan pengguna untuk menjadwalkan penutupan sistem atau melakukan penutupan segera.

## Usage
Berikut adalah sintaks asas untuk perintah `shutdown`:

```bash
shutdown [options] [arguments]
```

## Common Options
- `-h` : Mematikan sistem.
- `-r` : Merestart sistem.
- `-t` : Menentukan waktu dalam detik sebelum sistem dimatikan.
- `now` : Mematikan sistem serta-merta.
- `+m` : Menjadwalkan penutupan dalam m minit.

## Common Examples
1. **Mematikan sistem segera:**
   ```bash
   shutdown now
   ```

2. **Menjadwalkan penutupan dalam 5 minit:**
   ```bash
   shutdown +5
   ```

3. **Merestart sistem:**
   ```bash
   shutdown -r now
   ```

4. **Mematikan sistem pada waktu tertentu (contoh: 22:00):**
   ```bash
   shutdown 22:00
   ```

5. **Menghentikan penutupan yang telah dijadwalkan:**
   ```bash
   shutdown -c
   ```

## Tips
- Sentiasa simpan kerja anda sebelum menggunakan perintah `shutdown` untuk mengelakkan kehilangan data.
- Gunakan `shutdown -h now` untuk mematikan sistem dengan segera jika anda tidak memerlukan waktu penutupan.
- Untuk pengguna yang mempunyai akses root, pertimbangkan untuk menggunakan perintah ini dengan hati-hati, terutamanya pada pelayan yang sedang beroperasi.