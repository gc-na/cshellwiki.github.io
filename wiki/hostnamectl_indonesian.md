# [Linux] Bash hostnamectl Penggunaan: Mengelola nama host sistem

## Overview
Perintah `hostnamectl` digunakan untuk mengelola dan menampilkan informasi tentang nama host dan pengaturan sistem pada sistem operasi berbasis Linux. Dengan perintah ini, pengguna dapat dengan mudah mengubah nama host, melihat informasi sistem, dan mengelola pengaturan jaringan.

## Usage
Berikut adalah sintaks dasar dari perintah `hostnamectl`:

```bash
hostnamectl [options] [arguments]
```

## Common Options
- `set-hostname`: Mengubah nama host sistem.
- `status`: Menampilkan informasi tentang nama host dan status sistem.
- `set-icon-name`: Mengatur nama ikon untuk sistem.
- `set-chassis`: Mengatur jenis sasis perangkat (misalnya, desktop, laptop, server).
- `set-deployment`: Mengatur jenis penyebaran perangkat (misalnya, production, test).

## Common Examples
Berikut adalah beberapa contoh penggunaan `hostnamectl`:

### Menampilkan Status Hostname
Untuk menampilkan informasi tentang nama host dan status sistem, gunakan perintah berikut:

```bash
hostnamectl status
```

### Mengubah Nama Host
Untuk mengubah nama host sistem, gunakan perintah berikut (gantilah `nama-baru` dengan nama host yang diinginkan):

```bash
sudo hostnamectl set-hostname nama-baru
```

### Mengatur Jenis Sasis
Untuk mengatur jenis sasis perangkat, gunakan perintah berikut:

```bash
sudo hostnamectl set-chassis laptop
```

### Mengatur Nama Ikon
Untuk mengatur nama ikon sistem, gunakan perintah berikut:

```bash
sudo hostnamectl set-icon-name komputer
```

## Tips
- Pastikan untuk menggunakan `sudo` saat mengubah nama host atau pengaturan lainnya yang memerlukan hak akses administratif.
- Setelah mengubah nama host, disarankan untuk me-reboot sistem agar perubahan dapat diterapkan sepenuhnya.
- Gunakan `hostnamectl status` secara berkala untuk memeriksa informasi sistem dan memastikan bahwa pengaturan Anda sudah benar.