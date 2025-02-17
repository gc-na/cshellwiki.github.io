# [Linux] Bash mountpoint: Memeriksa titik pemautan sistem fail

## Overview
Perintah `mountpoint` digunakan untuk memeriksa sama ada direktori tertentu adalah titik pemautan untuk sistem fail. Ini berguna untuk memastikan bahawa sistem fail yang telah dipautkan berfungsi dengan betul dan untuk mengelakkan kesilapan semasa mengakses data.

## Usage
Sintaks asas untuk perintah `mountpoint` adalah seperti berikut:

```bash
mountpoint [options] [arguments]
```

## Common Options
- `-q`: Mod senyap; tidak menghasilkan output jika direktori adalah titik pemautan.
- `-d`: Menunjukkan maklumat tentang titik pemautan jika ia adalah titik pemautan.
- `--help`: Menunjukkan bantuan dan maklumat tentang penggunaan perintah.

## Common Examples
1. Memeriksa sama ada direktori `/mnt/data` adalah titik pemautan:
   ```bash
   mountpoint /mnt/data
   ```

2. Menggunakan mod senyap untuk memeriksa titik pemautan tanpa output:
   ```bash
   mountpoint -q /mnt/data
   ```

3. Menunjukkan maklumat tentang titik pemautan:
   ```bash
   mountpoint -d /mnt/data
   ```

## Tips
- Gunakan pilihan `-q` jika anda hanya ingin mengetahui status tanpa output yang tidak perlu.
- Sentiasa pastikan bahawa anda mempunyai kebenaran yang sesuai untuk memeriksa direktori yang ingin anda semak.
- Perintah ini berguna dalam skrip untuk memastikan bahawa titik pemautan wujud sebelum melakukan operasi lanjut.