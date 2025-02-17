# [Linux] Bash whoami Penggunaan: Menunjukkan nama pengguna semasa

## Overview
Perintah `whoami` digunakan dalam Bash untuk memaparkan nama pengguna yang sedang aktif dalam sesi terminal. Ini berguna untuk memastikan identiti pengguna semasa, terutamanya dalam sistem yang mempunyai pelbagai pengguna.

## Usage
Sintaks asas untuk perintah `whoami` adalah seperti berikut:

```
whoami [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk perintah `whoami`:

- `--help`: Memaparkan bantuan dan maklumat penggunaan.
- `--version`: Menunjukkan versi perintah `whoami`.

## Common Examples
Berikut adalah beberapa contoh praktikal menggunakan perintah `whoami`:

1. **Menunjukkan nama pengguna semasa:**
   ```bash
   whoami
   ```

2. **Memaparkan bantuan untuk perintah:**
   ```bash
   whoami --help
   ```

3. **Menunjukkan versi perintah:**
   ```bash
   whoami --version
   ```

## Tips
- Gunakan `whoami` untuk memastikan anda sedang bekerja dengan akaun pengguna yang betul sebelum menjalankan perintah yang memerlukan keizinan tertentu.
- Perintah ini berguna dalam skrip untuk memeriksa identiti pengguna yang menjalankan skrip tersebut.