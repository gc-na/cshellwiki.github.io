# [Linux] Bash tmux Penggunaan: Manajemen terminal multiplexer

## Overview
`tmux` adalah sebuah terminal multiplexer yang memungkinkan pengguna untuk mengelola beberapa sesi terminal dalam satu jendela. Dengan `tmux`, Anda dapat membagi jendela terminal menjadi beberapa panel, menjalankan beberapa sesi secara bersamaan, dan bahkan terhubung kembali ke sesi yang telah ditinggalkan.

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
- `split-window`: Membagi jendela menjadi panel baru.

## Common Examples
Berikut adalah beberapa contoh penggunaan `tmux` yang umum:

1. **Membuat sesi baru:**
   ```bash
   tmux new -s nama_sesi
   ```

2. **Menghubungkan ke sesi yang sudah ada:**
   ```bash
   tmux attach -t nama_sesi
   ```

3. **Menampilkan daftar sesi yang sedang berjalan:**
   ```bash
   tmux list-sessions
   ```

4. **Membagi jendela menjadi dua panel:**
   ```bash
   tmux split-window
   ```

5. **Menghentikan sesi:**
   ```bash
   tmux kill-session -t nama_sesi
   ```

## Tips
- Gunakan kombinasi tombol `Ctrl + b` diikuti dengan `c` untuk membuat jendela baru dalam sesi `tmux`.
- Untuk berpindah antar jendela, gunakan `Ctrl + b` diikuti dengan nomor jendela.
- Simpan konfigurasi `tmux` Anda di file `.tmux.conf` untuk mengatur preferensi secara otomatis saat memulai `tmux`.