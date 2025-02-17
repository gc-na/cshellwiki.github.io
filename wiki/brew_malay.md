# [Linux] Bash brew Penggunaan: Mengurus pakej perisian

## Overview
Perintah `brew` adalah pengurus pakej yang popular untuk sistem operasi macOS dan Linux. Ia membolehkan pengguna untuk memasang, mengemas kini, dan mengurus perisian dengan mudah melalui baris arahan.

## Usage
Sintaks asas untuk menggunakan `brew` adalah seperti berikut:

```bash
brew [options] [arguments]
```

## Common Options
- `install`: Memasang pakej baru.
- `update`: Mengemas kini senarai pakej yang tersedia.
- `upgrade`: Mengemas kini pakej yang telah dipasang ke versi terbaru.
- `remove`: Menghapuskan pakej yang tidak lagi diperlukan.
- `list`: Menunjukkan senarai pakej yang telah dipasang.

## Common Examples
Berikut adalah beberapa contoh penggunaan `brew`:

### Memasang Pakej
Untuk memasang pakej, gunakan arahan berikut:
```bash
brew install nama_pakej
```
Contoh:
```bash
brew install wget
```

### Mengemas kini Senarai Pakej
Untuk mengemas kini senarai pakej yang tersedia, gunakan:
```bash
brew update
```

### Mengemas kini Pakej
Untuk mengemas kini semua pakej yang telah dipasang, gunakan:
```bash
brew upgrade
```

### Menghapuskan Pakej
Untuk menghapuskan pakej yang tidak diperlukan, gunakan:
```bash
brew remove nama_pakej
```
Contoh:
```bash
brew remove wget
```

### Menunjukkan Senarai Pakej
Untuk melihat senarai semua pakej yang telah dipasang, gunakan:
```bash
brew list
```

## Tips
- Sentiasa jalankan `brew update` sebelum memasang atau mengemas kini pakej untuk memastikan anda mempunyai senarai terkini.
- Gunakan `brew search nama_pakej` untuk mencari pakej yang tersedia sebelum memasangnya.
- Untuk mendapatkan maklumat lanjut tentang pakej tertentu, gunakan `brew info nama_pakej`.