# [Linux] Bash flatpak penggunaan: Mengurus aplikasi dalam kontena

## Overview
Perintah `flatpak` digunakan untuk mengurus aplikasi yang dipasang dalam kontena. Ia membolehkan pengguna untuk memasang, menghapus, dan mengemas kini aplikasi dengan cara yang terasing dari sistem operasi utama, menjadikannya lebih selamat dan mudah diurus.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah flatpak:

```bash
flatpak [options] [arguments]
```

## Common Options
- `install`: Memasang aplikasi dari repositori.
- `uninstall`: Menghapus aplikasi yang telah dipasang.
- `update`: Mengemas kini aplikasi yang telah dipasang.
- `list`: Menyenaraikan semua aplikasi yang dipasang.
- `run`: Menjalankan aplikasi yang dipasang.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah flatpak:

1. **Memasang aplikasi**:
   ```bash
   flatpak install flathub org.videolan.VLC
   ```

2. **Menghapus aplikasi**:
   ```bash
   flatpak uninstall org.videolan.VLC
   ```

3. **Mengemas kini aplikasi**:
   ```bash
   flatpak update org.videolan.VLC
   ```

4. **Menyenaraikan aplikasi yang dipasang**:
   ```bash
   flatpak list
   ```

5. **Menjalankan aplikasi**:
   ```bash
   flatpak run org.videolan.VLC
   ```

## Tips
- Sentiasa semak untuk kemas kini aplikasi dengan menggunakan `flatpak update` secara berkala.
- Gunakan `flatpak list --app` untuk hanya menyenaraikan aplikasi dan bukan runtuhan.
- Untuk mendapatkan maklumat lanjut tentang aplikasi tertentu, gunakan `flatpak info [application-id]`.