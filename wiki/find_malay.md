# [Linux] Bash find penggunaan: Mencari nama fail

## Overview
Perintah `find` dalam Bash digunakan untuk mencari fail dan direktori dalam sistem fail berdasarkan kriteria tertentu. Ia membolehkan pengguna mencari fail berdasarkan nama, jenis, saiz, tarikh, dan banyak lagi.

## Usage
Sintaks asas untuk perintah `find` adalah seperti berikut:

```
find [pilihan] [argumen]
```

## Common Options
- `-name`: Mencari fail berdasarkan nama.
- `-type`: Menentukan jenis fail (contohnya, `f` untuk fail biasa, `d` untuk direktori).
- `-size`: Mencari fail berdasarkan saiz.
- `-mtime`: Mencari fail berdasarkan tarikh diubah suai.
- `-exec`: Menjalankan perintah pada setiap fail yang dijumpai.

## Common Examples
Berikut adalah beberapa contoh praktikal menggunakan perintah `find`:

1. Mencari fail dengan nama tertentu:
   ```bash
   find /path/to/directory -name "fail.txt"
   ```

2. Mencari semua fail dalam direktori yang mempunyai sambungan `.jpg`:
   ```bash
   find /path/to/directory -name "*.jpg"
   ```

3. Mencari direktori sahaja:
   ```bash
   find /path/to/directory -type d
   ```

4. Mencari fail yang lebih besar daripada 1MB:
   ```bash
   find /path/to/directory -size +1M
   ```

5. Mencari fail yang diubah suai dalam 7 hari yang lalu:
   ```bash
   find /path/to/directory -mtime -7
   ```

6. Menjalankan perintah `rm` untuk menghapuskan semua fail `.tmp`:
   ```bash
   find /path/to/directory -name "*.tmp" -exec rm {} \;
   ```

## Tips
- Gunakan `-iname` untuk mencari nama fail tanpa menghiraukan huruf besar atau kecil.
- Sentiasa semak hasil sebelum menggunakan `-exec` untuk mengelakkan penghapusan fail yang tidak diingini.
- Untuk mempercepatkan pencarian, hadkan pencarian kepada direktori tertentu yang diketahui mengandungi fail yang dicari.