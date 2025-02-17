# [Linux] Bash lsblk Penggunaan: Menyenaraikan peranti blok

## Overview
Perintah `lsblk` digunakan untuk menyenaraikan semua peranti blok yang tersedia di sistem Linux. Ini termasuk cakera keras, pemacu USB, dan partition. Ia memberikan maklumat tentang struktur peranti, termasuk saiz dan jenis sistem fail.

## Usage
Sintaks asas untuk perintah `lsblk` adalah seperti berikut:

```bash
lsblk [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk `lsblk` beserta penjelasan ringkas:

- `-a`, `--all`: Menunjukkan semua peranti, termasuk yang tidak terpasang.
- `-f`, `--fs`: Menunjukkan maklumat sistem fail untuk setiap peranti.
- `-l`, `--list`: Menunjukkan output dalam format senarai.
- `-o`, `--output`: Menentukan kolum yang ingin ditunjukkan dalam output.
- `-n`, `--noheadings`: Menghilangkan tajuk kolum dalam output.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `lsblk`:

1. **Menyenaraikan semua peranti blok:**
   ```bash
   lsblk
   ```

2. **Menyenaraikan semua peranti termasuk yang tidak terpasang:**
   ```bash
   lsblk -a
   ```

3. **Menunjukkan maklumat sistem fail untuk setiap peranti:**
   ```bash
   lsblk -f
   ```

4. **Menunjukkan output dalam format senarai:**
   ```bash
   lsblk -l
   ```

5. **Menentukan kolum yang ingin ditunjukkan:**
   ```bash
   lsblk -o NAME,SIZE,TYPE,MOUNTPOINT
   ```

## Tips
- Gunakan pilihan `-f` untuk mendapatkan maklumat tambahan tentang sistem fail, yang berguna untuk pengurusan peranti.
- Pilihan `-n` boleh membantu menjadikan output lebih bersih, terutamanya jika anda hanya memerlukan data tanpa tajuk.
- Untuk skrip automasi, pertimbangkan untuk menggunakan pilihan `--json` untuk mendapatkan output dalam format JSON yang mudah diproses.