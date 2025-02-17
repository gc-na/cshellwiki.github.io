# [Linux] Bash nice Penggunaan: Mengubah keutamaan proses

## Overview
Perintah `nice` dalam Bash digunakan untuk mengubah keutamaan proses yang sedang berjalan. Dengan menggunakan `nice`, anda boleh menentukan berapa banyak sumber CPU yang akan diberikan kepada proses tertentu. Proses dengan nilai nice yang lebih rendah akan mendapat lebih banyak sumber, sementara proses dengan nilai nice yang lebih tinggi akan mendapat sumber yang lebih sedikit.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `nice`:

```bash
nice [options] [arguments]
```

## Common Options
- `-n, --adjustment=N`: Menetapkan nilai nice kepada N. Nilai N boleh positif atau negatif.
- `--help`: Menunjukkan bantuan untuk perintah nice.
- `--version`: Menunjukkan versi perintah nice.

## Common Examples
Berikut adalah beberapa contoh penggunaan `nice`:

1. Menjalankan proses dengan nilai nice default (0):
   ```bash
   nice myscript.sh
   ```

2. Menjalankan proses dengan nilai nice yang lebih tinggi (10):
   ```bash
   nice -n 10 myscript.sh
   ```

3. Menjalankan proses dengan nilai nice yang lebih rendah (-5):
   ```bash
   nice -n -5 myscript.sh
   ```

4. Menjalankan perintah `top` dengan nilai nice 15:
   ```bash
   nice -n 15 top
   ```

## Tips
- Gunakan nilai nice yang lebih rendah untuk proses yang memerlukan lebih banyak sumber CPU, seperti aplikasi pengeditan video.
- Sebaliknya, gunakan nilai nice yang lebih tinggi untuk proses latar belakang yang tidak memerlukan banyak sumber, seperti pemindahan fail besar.
- Sentiasa periksa keutamaan proses anda dengan menggunakan perintah `ps` untuk memastikan semuanya berjalan dengan baik.