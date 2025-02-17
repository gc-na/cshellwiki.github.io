# [Linux] Bash basename Penggunaan: Mengambil nama fail dari laluan

## Overview
Perintah `basename` dalam Bash digunakan untuk mengekstrak nama fail daripada laluan penuh. Ini berguna apabila anda ingin mendapatkan hanya nama fail tanpa direktori yang mengelilinginya.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `basename`:

```bash
basename [options] [arguments]
```

## Common Options
- `-a`: Memproses semua argumen yang diberikan dan mengeluarkan nama fail untuk setiap satu.
- `-s`: Mengeluarkan nama fail tanpa sambungan tertentu yang ditentukan.

## Common Examples

1. **Mengambil nama fail dari laluan penuh:**

```bash
basename /home/user/document.txt
```
Output:
```
document.txt
```

2. **Mengambil nama fail tanpa sambungan:**

```bash
basename /home/user/document.txt .txt
```
Output:
```
document
```

3. **Mengambil nama fail dari beberapa laluan:**

```bash
basename -a /home/user/file1.txt /home/user/file2.txt
```
Output:
```
file1.txt
file2.txt
```

4. **Mengambil nama fail tanpa sambungan dari beberapa laluan:**

```bash
basename -a /home/user/file1.txt /home/user/file2.txt .txt
```
Output:
```
file1
file2
```

## Tips
- Gunakan `basename` dalam skrip untuk memudahkan pengendalian fail dan direktori.
- Sentiasa ingat untuk menyertakan sambungan jika anda ingin mengeluarkan nama fail tanpa sambungan.
- Anda boleh menggabungkan `basename` dengan perintah lain menggunakan `|` untuk memproses output dengan lebih lanjut.