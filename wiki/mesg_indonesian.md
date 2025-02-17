# [Linux] Bash mesg Penggunaan: Mengatur izin pesan terminal

## Overview
Perintah `mesg` digunakan untuk mengatur izin bagi pengguna lain untuk mengirim pesan ke terminal Anda. Dengan menggunakan perintah ini, Anda dapat mengontrol apakah pengguna lain dapat mengirim pesan menggunakan perintah `write` atau `talk`.

## Usage
Berikut adalah sintaks dasar dari perintah `mesg`:

```bash
mesg [options] [arguments]
```

## Common Options
- `y` : Mengizinkan pengguna lain untuk mengirim pesan ke terminal Anda.
- `n` : Menolak izin bagi pengguna lain untuk mengirim pesan ke terminal Anda.
- `--help` : Menampilkan bantuan dan informasi tentang penggunaan perintah ini.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `mesg`:

1. **Mengizinkan pesan dari pengguna lain:**
   ```bash
   mesg y
   ```

2. **Menolak pesan dari pengguna lain:**
   ```bash
   mesg n
   ```

3. **Menampilkan status izin pesan saat ini:**
   ```bash
   mesg
   ```

## Tips
- Gunakan `mesg n` saat Anda tidak ingin terganggu oleh pesan dari pengguna lain, terutama saat bekerja di lingkungan yang ramai.
- Sebelum mengizinkan pesan, pastikan Anda siap untuk menerima pesan dari pengguna lain.
- Perintah `mesg` hanya berlaku untuk sesi terminal saat ini; Anda perlu mengatur ulang izin jika membuka terminal baru.