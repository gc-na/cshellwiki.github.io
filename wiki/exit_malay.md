# [Linux] Bash exit: Menghentikan skrip dengan kod keluar

## Overview
Perintah `exit` dalam Bash digunakan untuk menghentikan skrip atau sesi terminal dan mengembalikan kod keluar kepada sistem operasi. Kod keluar ini biasanya digunakan untuk menunjukkan sama ada skrip telah berjaya dijalankan atau tidak.

## Usage
Berikut adalah sintaks asas untuk perintah `exit`:

```bash
exit [options] [arguments]
```

## Common Options
- `n`: Menentukan kod keluar yang ingin dikembalikan. Jika tidak ditentukan, kod keluar terakhir yang dijalankan akan digunakan.
- `-`: Menggunakan kod keluar dari proses terakhir yang dijalankan.

## Common Examples

1. **Menghentikan skrip dengan kod keluar 0 (berjaya)**:
   ```bash
   #!/bin/bash
   echo "Skrip berjaya dijalankan."
   exit 0
   ```

2. **Menghentikan skrip dengan kod keluar 1 (tidak berjaya)**:
   ```bash
   #!/bin/bash
   echo "Skrip gagal dijalankan."
   exit 1
   ```

3. **Menggunakan kod keluar dari proses terakhir**:
   ```bash
   #!/bin/bash
   ls /folder_tidak_wujud
   exit
   ```

4. **Menghentikan sesi terminal**:
   ```bash
   exit
   ```

## Tips
- Sentiasa gunakan kod keluar yang jelas (0 untuk berjaya, 1 atau lebih untuk kesalahan) untuk memudahkan pengesanan masalah.
- Dalam skrip yang lebih kompleks, pertimbangkan untuk menggunakan `trap` untuk menangani kesalahan dan memastikan `exit` dipanggil dengan kod yang sesuai.
- Gunakan `exit` di akhir skrip untuk memastikan semua proses selesai dengan baik sebelum keluar.