# [Linux] Bash talk Penggunaan: Berbual dengan pengguna lain

## Overview
Perintah `talk` dalam Bash membolehkan pengguna berkomunikasi secara langsung dengan pengguna lain di sistem yang sama atau di rangkaian. Ia membuka sesi berbual di mana kedua-dua pengguna boleh menghantar mesej secara real-time.

## Usage
Sintaks asas bagi perintah `talk` adalah seperti berikut:

```bash
talk [options] [user]
```

## Common Options
- `-h`: Menunjukkan bantuan mengenai penggunaan perintah.
- `-s`: Menghantar mesej tanpa menunggu balasan.
- `-t`: Menentukan waktu tamat untuk sesi berbual.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `talk`:

1. **Memulakan sesi berbual dengan pengguna lain:**
   ```bash
   talk username
   ```

2. **Menggunakan pilihan untuk menghantar mesej tanpa menunggu balasan:**
   ```bash
   talk -s username
   ```

3. **Menunjukkan bantuan untuk perintah talk:**
   ```bash
   talk -h
   ```

4. **Menentukan waktu tamat untuk sesi berbual:**
   ```bash
   talk -t 10 username
   ```

## Tips
- Pastikan pengguna yang ingin anda ajak berbual sedang dalam sesi aktif di sistem.
- Gunakan pilihan `-s` jika anda ingin menghantar mesej tanpa perlu menunggu balasan, berguna untuk memberi maklumat cepat.
- Periksa sambungan rangkaian jika anda tidak dapat berhubung dengan pengguna lain di rangkaian.