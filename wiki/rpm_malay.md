# [Linux] Bash rpm Penggunaan: Mengurus pakej perisian

## Overview
Perintah `rpm` (Red Hat Package Manager) digunakan untuk mengurus dan mengendalikan pakej perisian dalam sistem berasaskan RPM, seperti Red Hat, CentOS, dan Fedora. Ia membolehkan pengguna untuk memasang, mengemas kini, mengeluarkan, dan menyemak pakej perisian dengan mudah.

## Usage
Berikut adalah sintaks asas untuk perintah `rpm`:

```bash
rpm [options] [arguments]
```

## Common Options
- `-i` : Memasang pakej baru.
- `-U` : Mengemas kini pakej yang sedia ada.
- `-e` : Mengeluarkan (uninstall) pakej.
- `-q` : Menyemak dan mendapatkan maklumat mengenai pakej.
- `-l` : Menunjukkan fail yang terdapat dalam pakej.
- `--force` : Memaksa pemasangan walaupun terdapat konflik.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `rpm`:

### Memasang Pakej
```bash
rpm -i nama-pakej.rpm
```

### Mengemas Kini Pakej
```bash
rpm -U nama-pakej.rpm
```

### Mengeluarkan Pakej
```bash
rpm -e nama-pakej
```

### Menyemak Pakej yang Dipasang
```bash
rpm -q nama-pakej
```

### Menunjukkan Fail dalam Pakej
```bash
rpm -ql nama-pakej
```

## Tips
- Sentiasa semak kebergantungan pakej sebelum memasang untuk mengelakkan masalah.
- Gunakan `--force` dengan berhati-hati, kerana ia boleh menyebabkan konflik dengan pakej lain.
- Untuk mendapatkan maklumat lanjut tentang pilihan yang tersedia, gunakan `rpm --help`.