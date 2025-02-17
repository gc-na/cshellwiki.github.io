# [Linux] Bash ssh Penggunaan: Menghubungkan ke pelayan jauh

## Overview
Perintah `ssh` (Secure Shell) digunakan untuk mengakses dan mengurus pelayan jauh dengan selamat. Ia membolehkan pengguna untuk log masuk ke sistem lain melalui rangkaian dengan menggunakan sambungan yang disulitkan.

## Usage
Sintaks asas untuk menggunakan `ssh` adalah seperti berikut:

```
ssh [options] [user@]hostname
```

## Common Options
- `-p [port]`: Menentukan nombor port yang digunakan untuk sambungan.
- `-i [file]`: Menggunakan fail kunci peribadi untuk pengesahan.
- `-v`: Mengaktifkan mod verbose untuk mendapatkan maklumat lebih lanjut tentang sambungan.
- `-X`: Mengaktifkan pemindahan X11 untuk aplikasi GUI.

## Common Examples
1. **Sambung ke pelayan dengan nama pengguna dan alamat IP:**
   ```bash
   ssh user@192.168.1.1
   ```

2. **Sambung ke pelayan pada port tertentu:**
   ```bash
   ssh -p 2222 user@hostname.com
   ```

3. **Sambung menggunakan kunci peribadi:**
   ```bash
   ssh -i ~/.ssh/id_rsa user@hostname.com
   ```

4. **Sambung dengan mod verbose:**
   ```bash
   ssh -v user@hostname.com
   ```

5. **Sambung dengan pemindahan X11:**
   ```bash
   ssh -X user@hostname.com
   ```

## Tips
- Sentiasa gunakan kunci peribadi untuk pengesahan yang lebih selamat berbanding kata laluan.
- Simpan kunci peribadi anda dalam direktori yang selamat dan tetapkan izin yang betul.
- Gunakan mod verbose (`-v`) untuk menyelesaikan masalah sambungan jika anda menghadapi sebarang isu.
- Jika sering menyambung ke pelayan yang sama, pertimbangkan untuk menambah entri dalam fail `~/.ssh/config` untuk kemudahan.