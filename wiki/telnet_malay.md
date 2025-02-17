# [Linux] Bash telnet: Menghubungkan ke pelayan melalui protokol Telnet

## Overview
Perintah `telnet` digunakan untuk menghubungkan ke pelayan jauh melalui protokol Telnet. Ia membolehkan pengguna untuk berinteraksi dengan pelayan secara langsung melalui baris arahan, yang berguna untuk menguji sambungan dan mengakses perkhidmatan tertentu.

## Usage
Sintaks asas untuk perintah `telnet` adalah seperti berikut:

```
telnet [options] [arguments]
```

## Common Options
- `-l username`: Menetapkan nama pengguna untuk log masuk ke pelayan.
- `-d`: Mengaktifkan mod debug untuk membantu menyelesaikan masalah sambungan.
- `-n tracefile`: Menyimpan jejak sambungan ke dalam fail yang ditentukan.

## Common Examples
1. **Menghubungkan ke pelayan tertentu:**
   ```bash
   telnet example.com 80
   ```
   Ini akan menghubungkan ke pelayan `example.com` pada port 80.

2. **Menggunakan nama pengguna untuk log masuk:**
   ```bash
   telnet -l user example.com
   ```
   Menghubungkan ke `example.com` dengan nama pengguna `user`.

3. **Mengaktifkan mod debug:**
   ```bash
   telnet -d example.com
   ```
   Menghubungkan ke `example.com` dengan mod debug diaktifkan.

4. **Menyimpan jejak sambungan:**
   ```bash
   telnet -n mytrace.log example.com
   ```
   Menghubungkan ke `example.com` dan menyimpan jejak sambungan ke dalam fail `mytrace.log`.

## Tips
- Pastikan pelayan yang anda sambungkan membenarkan sambungan Telnet, kerana banyak pelayan kini menggunakan protokol yang lebih selamat seperti SSH.
- Gunakan mod debug jika anda menghadapi masalah sambungan untuk mendapatkan maklumat tambahan tentang apa yang mungkin salah.
- Sentiasa tutup sesi Telnet dengan perintah `quit` untuk mengelakkan sesi terbuka yang tidak diperlukan.