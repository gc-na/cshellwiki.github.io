# [Sistem Operasi] C Shell (csh) tmux Penggunaan: Mengelola sesi terminal

## Overview
Perintah `tmux` adalah terminal multiplexer yang memungkinkan pengguna untuk menjalankan beberapa sesi terminal dalam satu jendela. Dengan `tmux`, Anda dapat membagi jendela terminal menjadi beberapa panel, beralih antara sesi, dan menjaga sesi tetap berjalan bahkan setelah Anda keluar dari terminal.

## Usage
Berikut adalah sintaks dasar untuk menggunakan `tmux`:

```bash
tmux [options] [arguments]
```

## Common Options
- `new`: Membuat sesi baru.
- `attach`: Menghubungkan kembali ke sesi yang sudah ada.
- `list-sessions`: Menampilkan daftar sesi yang sedang berjalan.
- `kill-session`: Menghentikan sesi yang sedang berjalan.
- `detach`: Memutuskan sesi saat ini dan kembali ke terminal.

## Common Examples
Berikut adalah beberapa contoh penggunaan `tmux`:

1. **Membuat sesi baru**:
   ```bash
   tmux new -s mysession
   ```

2. **Menghubungkan ke sesi yang sudah ada**:
   ```bash
   tmux attach -t mysession
   ```

3. **Menampilkan daftar sesi yang sedang berjalan**:
   ```bash
   tmux list-sessions
   ```

4. **Menghentikan sesi**:
   ```bash
   tmux kill-session -t mysession
   ```

5. **Memutuskan sesi**:
   ```bash
   Ctrl + b, d
   ```

## Tips
- Gunakan nama sesi yang deskriptif agar mudah diingat.
- Manfaatkan pembagian jendela untuk multitasking; Anda bisa membuka beberapa panel dalam satu sesi.
- Simpan konfigurasi `tmux` di file `.tmux.conf` untuk mengatur preferensi Anda secara permanen.