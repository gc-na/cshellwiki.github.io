# [Linux] Bash iostat Penggunaan: Memantau statistik input/output sistem

## Overview
Perintah `iostat` digunakan untuk memantau statistik input/output (I/O) sistem, termasuk penggunaan CPU dan statistik peranti penyimpanan. Ia membantu pengguna untuk menganalisis prestasi sistem dan mengenal pasti sebarang masalah berkaitan I/O.

## Usage
Sintaks asas untuk menggunakan `iostat` adalah seperti berikut:

```bash
iostat [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk `iostat` beserta penjelasan ringkas:

- `-c`: Menunjukkan statistik penggunaan CPU sahaja.
- `-d`: Menunjukkan statistik peranti I/O.
- `-x`: Menunjukkan statistik peranti I/O dengan maklumat tambahan.
- `-m`: Menunjukkan statistik dalam megabait.
- `-t`: Menunjukkan waktu dan tarikh dalam output.

## Common Examples
Berikut adalah beberapa contoh praktikal menggunakan `iostat`:

1. **Menunjukkan statistik CPU dan I/O:**

   ```bash
   iostat
   ```

2. **Menunjukkan statistik penggunaan CPU sahaja:**

   ```bash
   iostat -c
   ```

3. **Menunjukkan statistik peranti I/O dengan maklumat tambahan:**

   ```bash
   iostat -x
   ```

4. **Menunjukkan statistik dalam megabait:**

   ```bash
   iostat -m
   ```

5. **Menunjukkan statistik dengan waktu dan tarikh:**

   ```bash
   iostat -t
   ```

## Tips
- Gunakan `iostat` secara berkala untuk memantau prestasi sistem dan mengesan sebarang masalah I/O.
- Gabungkan `iostat` dengan alat pemantauan lain seperti `top` atau `vmstat` untuk analisis yang lebih mendalam.
- Simpan output `iostat` ke dalam fail untuk analisis lanjut dengan menggunakan pengalihan output, contohnya: `iostat > output.txt`.