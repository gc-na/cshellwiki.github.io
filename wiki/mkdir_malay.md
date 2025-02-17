# [Linux] Bash mkdir Penggunaan: Membuat direktori baru

## Overview
Perintah `mkdir` digunakan untuk membuat direktori baru dalam sistem fail. Ia membolehkan pengguna untuk mengatur dan menyusun fail dengan lebih baik dengan mencipta folder baru.

## Usage
Berikut adalah sintaks asas untuk perintah `mkdir`:

```
mkdir [options] [arguments]
```

## Common Options
- `-p`: Membuat direktori secara rekursif, termasuk direktori induk yang tidak wujud.
- `-v`: Menunjukkan maklumat tentang direktori yang telah dibuat.
- `-m`: Menetapkan izin untuk direktori yang baru dibuat menggunakan format octal.

## Common Examples
Berikut adalah beberapa contoh penggunaan `mkdir`:

1. **Membuat satu direktori baru:**
   ```bash
   mkdir direktori_baru
   ```

2. **Membuat beberapa direktori sekaligus:**
   ```bash
   mkdir direktori1 direktori2 direktori3
   ```

3. **Membuat direktori secara rekursif:**
   ```bash
   mkdir -p /path/to/direktori/baru
   ```

4. **Membuat direktori dengan izin tertentu:**
   ```bash
   mkdir -m 755 direktori_izin
   ```

5. **Menunjukkan maklumat tentang direktori yang dibuat:**
   ```bash
   mkdir -v direktori_info
   ```

## Tips
- Gunakan pilihan `-p` jika anda ingin membuat struktur direktori yang kompleks tanpa perlu membuat setiap direktori induk secara manual.
- Sentiasa periksa izin direktori yang anda buat untuk memastikan ia sesuai dengan keperluan akses pengguna lain.
- Gunakan pilihan `-v` untuk mendapatkan maklumat tambahan semasa membuat direktori, ini berguna untuk pengesahan.