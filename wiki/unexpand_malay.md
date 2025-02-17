# [Linux] Bash unexpand Penggunaan: Menukar ruang menjadi tab

## Overview
Perintah `unexpand` dalam Bash digunakan untuk menukar ruang kosong (spaces) dalam fail teks kepada tab. Ini berguna untuk mengurangkan saiz fail atau untuk mematuhi format tertentu yang memerlukan penggunaan tab.

## Usage
Sintaks asas untuk perintah `unexpand` adalah seperti berikut:

```
unexpand [options] [arguments]
```

## Common Options
- `-a` : Menukar semua ruang kepada tab, bukan hanya ruang yang berturutan.
- `-t N` : Menetapkan lebar tab kepada N ruang.
- `--help` : Menunjukkan bantuan untuk perintah ini.
- `--version` : Menunjukkan versi perintah `unexpand`.

## Common Examples
Berikut adalah beberapa contoh penggunaan `unexpand`:

1. Menukar ruang kepada tab dalam fail:
   ```bash
   unexpand input.txt > output.txt
   ```

2. Menukar semua ruang kepada tab:
   ```bash
   unexpand -a input.txt > output.txt
   ```

3. Menetapkan lebar tab kepada 4 ruang:
   ```bash
   unexpand -t 4 input.txt > output.txt
   ```

4. Melihat hasil tanpa menyimpan ke dalam fail:
   ```bash
   unexpand input.txt
   ```

## Tips
- Sentiasa buat salinan fail asal sebelum menggunakan `unexpand` untuk mengelakkan kehilangan data.
- Gunakan pilihan `-t` untuk menyesuaikan lebar tab mengikut keperluan format anda.
- Periksa hasil akhir dengan menggunakan `cat` atau `less` untuk memastikan format yang diingini.