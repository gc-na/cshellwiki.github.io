# [Linux] Bash renice: Mengubah prioritas proses

## Overview
Perintah `renice` digunakan untuk mengubah prioritas dari proses yang sedang berjalan di sistem operasi Linux. Dengan mengubah prioritas, Anda dapat mengatur seberapa banyak sumber daya CPU yang diberikan kepada proses tertentu, yang dapat membantu dalam pengelolaan kinerja sistem.

## Usage
Berikut adalah sintaks dasar dari perintah `renice`:

```bash
renice [options] [arguments]
```

## Common Options
- `-n, --priority <nilai>`: Menentukan nilai prioritas baru. Nilai dapat berkisar dari -20 (prioritas tertinggi) hingga 19 (prioritas terendah).
- `-p, --pid <pid>`: Menentukan ID proses yang ingin diubah prioritasnya.
- `-g, --pgroup <pgid>`: Mengubah prioritas semua proses dalam grup proses tertentu.
- `-u, --user <user>`: Mengubah prioritas semua proses yang dimiliki oleh pengguna tertentu.

## Common Examples
Berikut adalah beberapa contoh penggunaan `renice`:

1. Mengubah prioritas proses dengan ID 1234 menjadi 10:
   ```bash
   renice -n 10 -p 1234
   ```

2. Mengubah prioritas semua proses yang dimiliki oleh pengguna `john` menjadi -5:
   ```bash
   renice -n -5 -u john
   ```

3. Mengubah prioritas semua proses dalam grup proses dengan ID 5678 menjadi 0:
   ```bash
   renice -n 0 -g 5678
   ```

4. Menampilkan prioritas saat ini dari proses dengan ID 1234:
   ```bash
   ps -o pid,ni,cmd -p 1234
   ```

## Tips
- Gunakan `renice` dengan hati-hati, karena mengubah prioritas proses dapat mempengaruhi kinerja sistem secara keseluruhan.
- Sebaiknya gunakan nilai prioritas negatif hanya untuk proses yang sangat penting, agar tidak mengganggu proses lain.
- Anda memerlukan hak akses yang sesuai (misalnya, superuser) untuk mengubah prioritas proses yang bukan milik Anda.