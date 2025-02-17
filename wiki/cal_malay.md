# [Linux] Bash cal Penggunaan: Menunjukkan kalendar

## Overview
Perintah `cal` digunakan untuk memaparkan kalendar dalam format teks. Ia membolehkan pengguna melihat bulan atau tahun tertentu dengan mudah, serta mengetahui hari-hari dalam bulan tersebut.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `cal`:

```
cal [options] [arguments]
```

## Common Options
- `-m` : Menunjukkan kalendar dengan bulan semasa di tengah.
- `-y` : Menunjukkan kalendar untuk tahun semasa.
- `-3` : Menunjukkan kalendar untuk bulan semasa, bulan sebelumnya, dan bulan seterusnya.
- `-j` : Menunjukkan hari julian (hari ke- dalam tahun).
- `-A <n>` : Menunjukkan n bulan selepas bulan semasa.
- `-B <n>` : Menunjukkan n bulan sebelum bulan semasa.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `cal`:

1. Menunjukkan kalendar untuk bulan semasa:
   ```bash
   cal
   ```

2. Menunjukkan kalendar untuk bulan tertentu (contohnya, Mac 2023):
   ```bash
   cal 03 2023
   ```

3. Menunjukkan kalendar untuk tahun semasa:
   ```bash
   cal -y
   ```

4. Menunjukkan kalendar untuk bulan semasa dan bulan sebelum serta selepas:
   ```bash
   cal -3
   ```

5. Menunjukkan kalendar dengan hari julian:
   ```bash
   cal -j
   ```

## Tips
- Gunakan `cal -m` untuk mendapatkan pandangan yang lebih baik dengan bulan semasa di tengah.
- Untuk merancang aktiviti, gunakan `cal -A 1` untuk melihat bulan semasa dan bulan seterusnya.
- Jika anda ingin mencetak kalendar, pertimbangkan untuk mengalihkan output ke fail menggunakan `>`, contohnya: `cal > kalendar.txt`.