# [Linux] Bash groups penggunaan: Menampilkan grup pengguna

## Overview
Perintah `groups` digunakan untuk menampilkan grup-grup yang menjadi anggota dari pengguna tertentu. Jika tidak ada nama pengguna yang diberikan, perintah ini akan menampilkan grup untuk pengguna yang sedang aktif saat ini.

## Usage
Berikut adalah sintaks dasar dari perintah `groups`:

```bash
groups [options] [arguments]
```

## Common Options
- `-h`, `--help`: Menampilkan bantuan tentang penggunaan perintah ini.
- `-V`, `--version`: Menampilkan versi dari perintah `groups`.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `groups`:

1. Menampilkan grup untuk pengguna yang sedang aktif:
   ```bash
   groups
   ```

2. Menampilkan grup untuk pengguna tertentu, misalnya `john`:
   ```bash
   groups john
   ```

3. Menampilkan grup untuk beberapa pengguna sekaligus:
   ```bash
   groups alice bob charlie
   ```

4. Menampilkan grup dengan opsi bantuan:
   ```bash
   groups --help
   ```

## Tips
- Gunakan perintah `groups` tanpa argumen untuk dengan cepat memeriksa grup pengguna yang sedang aktif.
- Jika Anda ingin mengetahui grup untuk pengguna lain, pastikan Anda memiliki izin yang diperlukan untuk melihat informasi tersebut.
- Perintah ini sangat berguna dalam manajemen sistem untuk memastikan pengguna memiliki akses ke grup yang tepat.