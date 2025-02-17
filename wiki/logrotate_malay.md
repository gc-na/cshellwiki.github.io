# [Linux] Bash logrotate: Mengurus dan memutar log

## Overview
Perintah `logrotate` digunakan untuk mengurus fail log sistem dengan cara memutar, mengompres, dan menghapus fail log yang lama. Ini membantu dalam mengelakkan penggunaan ruang cakera yang berlebihan dan memastikan fail log tetap teratur.

## Usage
Berikut adalah sintaks asas untuk perintah `logrotate`:

```bash
logrotate [options] [arguments]
```

## Common Options
- `-f`: Memaksa logrotate untuk memutar log walaupun tidak diperlukan.
- `-s`: Menentukan fail status yang digunakan untuk menyimpan maklumat tentang log yang telah diputar.
- `-v`: Mengaktifkan mod verbose untuk menunjukkan maklumat lanjut semasa proses pemutaran.
- `-d`: Mod debug yang menunjukkan apa yang akan dilakukan tanpa melaksanakannya.

## Common Examples
1. **Memutar log menggunakan fail konfigurasi lalai:**
   ```bash
   logrotate /etc/logrotate.conf
   ```

2. **Memaksa pemutaran log:**
   ```bash
   logrotate -f /etc/logrotate.conf
   ```

3. **Menjalankan logrotate dalam mod verbose:**
   ```bash
   logrotate -v /etc/logrotate.conf
   ```

4. **Menggunakan fail status khusus:**
   ```bash
   logrotate -s /var/lib/logrotate/status /etc/logrotate.conf
   ```

## Tips
- Pastikan untuk mengkonfigurasi fail logrotate dengan betul untuk mengelakkan kehilangan data log penting.
- Selalu uji konfigurasi baru menggunakan mod debug (`-d`) sebelum melaksanakannya secara langsung.
- Jadwalkan logrotate untuk dijalankan secara berkala menggunakan cron untuk memastikan pemutaran log dilakukan secara automatik.