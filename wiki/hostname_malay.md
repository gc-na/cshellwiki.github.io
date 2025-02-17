# [Linux] Bash hostname penggunaan: Menetapkan dan memaparkan nama host

## Overview
Perintah `hostname` digunakan untuk memaparkan atau menetapkan nama host sistem. Nama host adalah nama unik yang diberikan kepada komputer dalam rangkaian, membolehkannya dikenali oleh peranti lain.

## Usage
Berikut adalah sintaks asas untuk perintah `hostname`:

```
hostname [options] [arguments]
```

## Common Options
- `-f`, `--fqdn`: Memaparkan nama host sepenuhnya (Fully Qualified Domain Name).
- `-i`, `--ip-address`: Memaparkan alamat IP untuk nama host.
- `-s`, `--short`: Memaparkan nama host pendek tanpa domain.
- `-A`, `--all-fqdns`: Memaparkan semua nama host sepenuhnya yang berkaitan dengan sistem.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `hostname`:

### 1. Memaparkan nama host semasa
```bash
hostname
```

### 2. Memaparkan nama host sepenuhnya
```bash
hostname -f
```

### 3. Memaparkan alamat IP untuk nama host
```bash
hostname -i
```

### 4. Menetapkan nama host baru
```bash
sudo hostname new-hostname
```

### 5. Memaparkan nama host pendek
```bash
hostname -s
```

## Tips
- Sentiasa gunakan `sudo` apabila menetapkan nama host baru untuk memastikan anda mempunyai kebenaran yang diperlukan.
- Selepas menetapkan nama host, pertimbangkan untuk mengubah fail `/etc/hostname` untuk memastikan perubahan kekal selepas reboot.
- Gunakan `hostname -A` untuk melihat semua nama host sepenuhnya jika sistem anda mempunyai beberapa nama domain.