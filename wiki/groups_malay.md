# [Linux] Bash groups: Menunjukkan keahlian pengguna dalam kumpulan

## Overview
Perintah `groups` dalam Bash digunakan untuk menunjukkan kumpulan (group) yang menjadi keahlian bagi pengguna tertentu. Ia memberikan maklumat tentang kumpulan yang dianggotai oleh pengguna, yang boleh berguna untuk pengurusan akses dan keselamatan dalam sistem Linux.

## Usage
Sintaks asas untuk perintah `groups` adalah seperti berikut:

```
groups [options] [arguments]
```

## Common Options
- `-a`: Menunjukkan semua kumpulan yang dianggotai oleh pengguna, termasuk yang tidak aktif.
- `--help`: Menunjukkan maklumat bantuan tentang perintah `groups`.
- `--version`: Menunjukkan versi perintah `groups`.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan perintah `groups`:

1. **Menunjukkan kumpulan untuk pengguna semasa:**
   ```bash
   groups
   ```

2. **Menunjukkan kumpulan untuk pengguna tertentu:**
   ```bash
   groups username
   ```

3. **Menunjukkan semua kumpulan termasuk yang tidak aktif:**
   ```bash
   groups -a username
   ```

4. **Mendapatkan maklumat bantuan:**
   ```bash
   groups --help
   ```

## Tips
- Gunakan perintah `groups` tanpa argumen untuk cepat mengetahui kumpulan yang anda sertai.
- Jika anda menguruskan pelayan, periksa kumpulan pengguna secara berkala untuk memastikan keselamatan dan akses yang betul.
- Kombinasikan perintah `groups` dengan perintah lain seperti `id` untuk mendapatkan maklumat lebih lanjut mengenai pengguna dan keahlian mereka.