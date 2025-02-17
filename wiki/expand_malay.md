# [Linux] Bash expand penggunaan: Menukar tab kepada ruang

## Overview
Perintah `expand` dalam Bash digunakan untuk menukar karakter tab dalam fail teks kepada ruang. Ini berguna untuk memastikan keseragaman dalam pemformatan teks, terutamanya apabila bekerja dengan fail yang mungkin mengandungi tab yang berbeza-beza.

## Usage
Sintaks asas bagi perintah `expand` adalah seperti berikut:

```bash
expand [options] [arguments]
```

## Common Options
- `-t, --tabs=N` : Menetapkan lebar tab kepada N ruang.
- `-i, --initial` : Mengubah hanya tab yang muncul selepas teks yang telah diproses.
- `-n, --no-tabs` : Mengeluarkan semua tab tanpa menggantikannya dengan ruang.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `expand`:

1. **Menukar tab kepada ruang dalam fail:**
   ```bash
   expand fail.txt
   ```

2. **Menetapkan lebar tab kepada 4 ruang:**
   ```bash
   expand -t 4 fail.txt
   ```

3. **Menggunakan pilihan `-i` untuk hanya mengubah tab selepas teks:**
   ```bash
   expand -i fail.txt
   ```

4. **Mengeluarkan semua tab tanpa menggantikannya:**
   ```bash
   expand -n fail.txt
   ```

## Tips
- Sentiasa semak fail output selepas menggunakan `expand` untuk memastikan pemformatan adalah seperti yang diinginkan.
- Gunakan pilihan `-t` untuk menyesuaikan lebar tab mengikut keperluan projek anda.
- Jika anda ingin menyimpan hasil ke dalam fail baru, gunakan pengalihan output:
  ```bash
  expand fail.txt > fail_baru.txt
  ```