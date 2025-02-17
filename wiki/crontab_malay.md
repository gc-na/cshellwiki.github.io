# [Linux] Bash crontab Penggunaan: Menjadwalkan Tugas

## Overview
Perintah `crontab` digunakan untuk menjadwalkan tugas-tugas yang akan dijalankan secara automatik pada waktu tertentu di sistem operasi Linux. Dengan menggunakan `crontab`, pengguna dapat mengatur skrip atau perintah untuk dijalankan secara berkala, seperti setiap jam, setiap hari, atau pada waktu tertentu.

## Usage
Berikut adalah sintaks asas untuk perintah `crontab`:

```bash
crontab [options] [arguments]
```

## Common Options
- `-e`: Mengedit fail crontab pengguna semasa.
- `-l`: Menyenaraikan semua tugas yang dijadwalkan dalam crontab.
- `-r`: Menghapus fail crontab pengguna semasa.
- `-i`: Meminta pengesahan sebelum menghapus fail crontab.

## Common Examples
Berikut adalah beberapa contoh penggunaan `crontab`:

1. **Menjadwalkan skrip untuk dijalankan setiap hari pada jam 2 pagi:**
   ```bash
   0 2 * * * /path/to/script.sh
   ```

2. **Menjalankan perintah `backup.sh` setiap hari pada jam 3 petang:**
   ```bash
   0 15 * * * /path/to/backup.sh
   ```

3. **Menjalankan perintah setiap 5 minit:**
   ```bash
   */5 * * * * /path/to/command
   ```

4. **Menjalankan perintah pada hari Ahad setiap minggu pada jam 6 petang:**
   ```bash
   0 18 * * 0 /path/to/weekly_task.sh
   ```

## Tips
- Sentiasa semak log untuk memastikan tugas dijalankan seperti yang dirancang.
- Gunakan `crontab -l` untuk menyemak semua tugas yang telah anda jadwalkan.
- Pastikan skrip atau perintah yang dijadwalkan mempunyai izin eksekusi yang betul.
- Gunakan path penuh untuk skrip atau perintah untuk mengelakkan masalah dengan direktori kerja.