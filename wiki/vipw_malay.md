# [Linux] Bash vipw Penggunaan: Mengedit fail passwd dengan selamat

## Overview
Perintah `vipw` digunakan untuk mengedit fail `passwd` dan `group` dalam sistem Unix/Linux dengan cara yang selamat. Ia memastikan bahawa fail-fail ini tidak diubahsuai secara serentak oleh lebih daripada satu pengguna, yang dapat mengelakkan kerosakan pada sistem pengguna.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `vipw`:

```bash
vipw [options]
```

## Common Options
- `-s`: Mengedit fail `shadow` yang berkaitan dengan pengguna.
- `-g`: Mengedit fail `group` untuk pengurusan kumpulan pengguna.
- `-m`: Mengedit fail `passwd` dan `group` secara serentak.

## Common Examples
1. **Mengedit fail passwd**:
   ```bash
   vipw
   ```

2. **Mengedit fail group**:
   ```bash
   vipw -g
   ```

3. **Mengedit fail shadow**:
   ```bash
   vipw -s
   ```

4. **Mengedit fail passwd dan group secara serentak**:
   ```bash
   vipw -m
   ```

## Tips
- Sentiasa gunakan `vipw` untuk mengedit fail `passwd` dan `group` bagi memastikan keselamatan dan integriti sistem.
- Pastikan anda mempunyai hak akses yang sesuai sebelum menggunakan `vipw`.
- Setelah selesai mengedit, periksa semula perubahan anda untuk mengelakkan kesilapan yang boleh menyebabkan masalah log masuk pengguna.