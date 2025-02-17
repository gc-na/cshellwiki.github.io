# [Linux] Bash sftp Penggunaan: Memindahkan fail secara selamat

## Overview
Perintah `sftp` (Secure File Transfer Protocol) digunakan untuk memindahkan fail antara komputer melalui sambungan yang selamat. Ia adalah sebahagian daripada suite SSH dan membolehkan pengguna untuk mengakses dan mengurus fail pada pelayan jarak jauh dengan cara yang selamat.

## Usage
Berikut adalah sintaks asas untuk perintah `sftp`:

```bash
sftp [options] [user@]host
```

## Common Options
- `-P port`: Menentukan nombor port untuk sambungan.
- `-i identity_file`: Menggunakan fail identiti tertentu untuk pengesahan.
- `-o option`: Menetapkan pilihan tambahan untuk sambungan.
- `-b batchfile`: Menggunakan fail batch untuk menjalankan perintah secara automatik.

## Common Examples
Berikut adalah beberapa contoh penggunaan `sftp`:

1. **Sambung ke pelayan SFTP:**
   ```bash
   sftp user@hostname
   ```

2. **Sambung ke pelayan SFTP menggunakan port tertentu:**
   ```bash
   sftp -P 2222 user@hostname
   ```

3. **Muat naik fail ke pelayan:**
   ```bash
   sftp user@hostname
   put localfile.txt
   ```

4. **Muat turun fail dari pelayan:**
   ```bash
   sftp user@hostname
   get remotefile.txt
   ```

5. **Menyenaraikan fail dalam direktori pelayan:**
   ```bash
   sftp user@hostname
   ls
   ```

## Tips
- Sentiasa gunakan sambungan yang selamat dengan `sftp` untuk melindungi data anda.
- Gunakan fail identiti untuk pengesahan yang lebih selamat dan mudah.
- Jika anda sering menggunakan `sftp`, pertimbangkan untuk menyimpan maklumat pelayan dalam fail konfigurasi SSH untuk kemudahan akses.