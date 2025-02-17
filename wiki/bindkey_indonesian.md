# [Linux] Bash bindkey Penggunaan: Mengatur pintasan keyboard di shell

## Overview
Perintah `bindkey` digunakan untuk mengatur dan mengelola pintasan keyboard di shell, terutama dalam lingkungan yang menggunakan Zsh. Dengan `bindkey`, pengguna dapat mengonfigurasi bagaimana kombinasi tombol tertentu berfungsi, meningkatkan efisiensi saat bekerja di terminal.

## Usage
Berikut adalah sintaks dasar dari perintah `bindkey`:

```bash
bindkey [options] [arguments]
```

## Common Options
- `-L`: Menampilkan daftar semua pintasan yang terikat saat ini.
- `-d`: Mengatur mode default untuk pintasan.
- `-e`: Mengatur mode Emacs untuk pintasan.
- `-v`: Mengatur mode Vi untuk pintasan.

## Common Examples
Berikut adalah beberapa contoh penggunaan `bindkey`:

1. **Menampilkan semua pintasan yang terikat**:
   ```bash
   bindkey -L
   ```

2. **Mengatur pintasan untuk menghapus karakter sebelum kursor**:
   ```bash
   bindkey '^H' backward-delete-char
   ```

3. **Mengatur pintasan untuk menjalankan perintah tertentu**:
   ```bash
   bindkey '^X^R' run-command
   ```

4. **Mengatur mode Vi untuk pintasan**:
   ```bash
   bindkey -v
   ```

## Tips
- Selalu periksa pintasan yang sudah ada dengan `bindkey -L` sebelum menambahkan yang baru untuk menghindari konflik.
- Gunakan mode yang sesuai (Emacs atau Vi) sesuai dengan preferensi Anda untuk pengalaman yang lebih nyaman.
- Simpan konfigurasi `bindkey` Anda di file `.zshrc` agar tetap berlaku setiap kali Anda membuka terminal baru.