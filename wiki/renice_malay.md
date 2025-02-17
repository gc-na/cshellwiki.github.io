# [Linux] Bash renice Penggunaan: Mengubah keutamaan proses

## Overview
Perintah `renice` digunakan untuk mengubah keutamaan proses yang sedang berjalan di sistem Linux. Keutamaan ini menentukan seberapa banyak sumber daya CPU yang diberikan kepada proses tersebut. Proses dengan keutamaan yang lebih rendah akan mendapat lebih banyak sumber daya, manakala proses dengan keutamaan yang lebih tinggi akan mendapat kurang.

## Usage
Sintaks asas untuk menggunakan perintah `renice` adalah seperti berikut:

```
renice [options] [arguments]
```

## Common Options
- `-n, --priority`: Menentukan nilai keutamaan baru. Nilai boleh antara -20 (keutamaan tertinggi) hingga 19 (keutamaan terendah).
- `-p, --pid`: Mengubah keutamaan proses berdasarkan ID proses (PID).
- `-g, --pgrp`: Mengubah keutamaan semua proses dalam kumpulan proses tertentu.
- `-u, --user`: Mengubah keutamaan semua proses yang dimiliki oleh pengguna tertentu.

## Common Examples
1. Mengubah keutamaan proses dengan PID 1234 kepada 10:
   ```bash
   renice 10 -p 1234
   ```

2. Mengubah keutamaan semua proses milik pengguna "john" kepada -5:
   ```bash
   renice -5 -u john
   ```

3. Mengubah keutamaan semua proses dalam kumpulan proses dengan ID 5678 kepada 0:
   ```bash
   renice 0 -g 5678
   ```

4. Mengetahui keutamaan proses tertentu sebelum mengubahnya:
   ```bash
   ps -o pid,ni,cmd -p 1234
   ```

## Tips
- Sebaiknya gunakan nilai keutamaan yang lebih tinggi (nilai negatif) untuk proses yang memerlukan lebih banyak sumber daya, seperti aplikasi yang memerlukan pemprosesan intensif.
- Sentiasa semak keutamaan proses selepas mengubahnya untuk memastikan bahawa perubahan telah berjaya.
- Hanya pengguna dengan hak istimewa yang boleh mengubah keutamaan proses yang dimiliki oleh pengguna lain.