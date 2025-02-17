# [Linux] Bash screen penggunaan: Mengurus sesi terminal

## Overview
Perintah `screen` adalah alat yang berguna dalam sistem operasi Linux yang membolehkan pengguna untuk menjalankan sesi terminal secara berasingan. Ia membolehkan anda untuk menjalankan aplikasi di latar belakang dan menyambung semula ke sesi tersebut pada bila-bila masa, walaupun anda terputus dari sambungan.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah screen:

```bash
screen [options] [arguments]
```

## Common Options
- `-S [nama]`: Memberi nama kepada sesi baru yang akan dicipta.
- `-d -r [nama]`: Memutuskan sambungan sesi yang sedang berjalan dan menyambung semula ke sesi tersebut.
- `-list`: Menunjukkan senarai sesi screen yang sedang berjalan.
- `-L`: Mengaktifkan log fail untuk sesi screen.

## Common Examples
Berikut adalah beberapa contoh praktikal menggunakan perintah screen:

1. **Mencipta sesi baru dengan nama:**
   ```bash
   screen -S sesi_saya
   ```

2. **Menyambung semula ke sesi yang telah ditinggalkan:**
   ```bash
   screen -d -r sesi_saya
   ```

3. **Melihat senarai sesi yang sedang berjalan:**
   ```bash
   screen -list
   ```

4. **Mengaktifkan log untuk sesi:**
   ```bash
   screen -L
   ```

## Tips
- Sentiasa beri nama kepada sesi anda menggunakan `-S` untuk memudahkan pengurusan.
- Gunakan `Ctrl + A` diikuti dengan `D` untuk memutuskan sambungan dari sesi tanpa menutupnya.
- Pastikan untuk memeriksa log fail jika anda perlu merujuk kepada output dari sesi yang telah dijalankan.