# [Linux] Bash tmux Penggunaan: Mengurus sesi terminal

## Overview
`tmux` adalah alat terminal multiplexer yang membolehkan pengguna untuk menjalankan beberapa sesi terminal dalam satu jendela. Ia membolehkan pengguna untuk membahagikan jendela terminal, menyimpan sesi, dan beralih antara sesi dengan mudah. Ini sangat berguna untuk pengaturcara dan pentadbir sistem yang memerlukan akses kepada beberapa proses sekaligus.

## Usage
Berikut adalah sintaks asas untuk menggunakan `tmux`:

```
tmux [options] [arguments]
```

## Common Options
- `new`: Membuat sesi baru.
- `attach`: Menyambung ke sesi yang sudah ada.
- `list-sessions`: Menyenaraikan semua sesi yang sedang berjalan.
- `kill-session`: Menamatkan sesi yang sedang berjalan.
- `detach`: Memisahkan sesi semasa tanpa menamatkannya.

## Common Examples
Berikut adalah beberapa contoh penggunaan `tmux`:

### Membuat Sesi Baru
```bash
tmux new -s mysession
```

### Menyambung ke Sesi yang Sudah Ada
```bash
tmux attach -t mysession
```

### Menyenaraikan Semua Sesi
```bash
tmux list-sessions
```

### Menamatkan Sesi
```bash
tmux kill-session -t mysession
```

### Memisahkan Sesi
```bash
Ctrl-b d
```

## Tips
- Gunakan nama sesi yang deskriptif untuk memudahkan pengenalan.
- Simpan sesi yang sedang berjalan dengan menggunakan `detach` agar tidak kehilangan kerja yang sedang dilakukan.
- Pelajari pintasan keyboard `tmux` untuk meningkatkan produktiviti, seperti `Ctrl-b %` untuk membahagikan jendela secara menegak.