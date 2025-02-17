# [Linux] Bash htop Penggunaan: Memantau penggunaan sumber sistem

## Overview
Perintah `htop` adalah alat pemantauan interaktif yang membolehkan pengguna melihat penggunaan sumber sistem secara real-time. Ia memberikan pandangan yang lebih baik dan lebih mudah dibaca berbanding dengan perintah `top`, dengan ciri-ciri tambahan seperti kemampuan untuk menavigasi dan mengurus proses.

## Usage
Sintaks asas untuk menggunakan `htop` adalah seperti berikut:

```bash
htop [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan umum untuk `htop`:

- `-d <delay>`: Menetapkan kelewatan antara kemas kini dalam milisaat.
- `-u <user>`: Menunjukkan hanya proses yang dijalankan oleh pengguna tertentu.
- `-p <pid>`: Memaparkan hanya proses dengan ID proses tertentu.
- `--help`: Memaparkan maklumat bantuan tentang penggunaan `htop`.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `htop`:

1. **Menjalankan htop secara asas**:
   ```bash
   htop
   ```

2. **Menetapkan kelewatan kemas kini kepada 2 saat**:
   ```bash
   htop -d 2
   ```

3. **Menunjukkan proses untuk pengguna tertentu**:
   ```bash
   htop -u username
   ```

4. **Menunjukkan proses tertentu dengan ID**:
   ```bash
   htop -p 1234
   ```

## Tips
- Gunakan kekunci anak panah untuk menavigasi antara proses dan tekan `F9` untuk membunuh proses yang dipilih.
- Anda boleh menyaring proses dengan menekan `F3` dan memasukkan nama proses.
- Untuk menyimpan konfigurasi htop, tekan `F2` untuk membuka menu setup dan simpan perubahan yang anda buat.