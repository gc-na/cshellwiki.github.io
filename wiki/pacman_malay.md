# [Linux] Bash pacman Penggunaan: Mengurus pakej dalam sistem

## Overview
Perintah `pacman` adalah pengurus pakej yang digunakan dalam sistem operasi berasaskan Arch Linux. Ia membolehkan pengguna untuk memasang, mengemas kini, dan menghapuskan pakej perisian dengan mudah.

## Usage
Sintaks asas untuk menggunakan `pacman` adalah seperti berikut:

```bash
pacman [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa yang digunakan dengan `pacman`:

- `-S`: Pasang pakej.
- `-R`: Buang pakej.
- `-U`: Pasang pakej dari fail.
- `-Sy`: Kemas kini pangkalan data pakej.
- `-Syu`: Kemas kini sistem dan semua pakej.

## Common Examples
Berikut adalah beberapa contoh penggunaan `pacman`:

1. **Pasang pakej**:
   ```bash
   pacman -S nama_pakej
   ```

2. **Buang pakej**:
   ```bash
   pacman -R nama_pakej
   ```

3. **Kemas kini pangkalan data pakej**:
   ```bash
   pacman -Sy
   ```

4. **Kemas kini semua pakej dalam sistem**:
   ```bash
   pacman -Syu
   ```

5. **Pasang pakej dari fail**:
   ```bash
   pacman -U /path/to/file.pkg.tar.zst
   ```

## Tips
- Sentiasa gunakan `-Syu` untuk memastikan sistem anda sentiasa dikemas kini.
- Sebelum membuang pakej, periksa jika terdapat kebergantungan yang mungkin terjejas.
- Gunakan `pacman -Q` untuk menyemak senarai pakej yang telah dipasang dalam sistem anda.