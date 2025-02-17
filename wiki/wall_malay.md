# [Linux] Bash wall penggunaan: Menghantar mesej kepada semua pengguna

## Overview
Perintah `wall` digunakan untuk menghantar mesej kepada semua pengguna yang sedang log masuk ke sistem Linux. Mesej ini akan dipaparkan di terminal mereka, membolehkan pentadbir sistem atau pengguna lain untuk menyampaikan maklumat penting dengan cepat.

## Usage
Sintaks asas untuk perintah `wall` adalah seperti berikut:

```bash
wall [options] [arguments]
```

## Common Options
- `-n` : Tidak menghantar mesej kepada pengguna yang tidak aktif.
- `-s` : Menghantar mesej tanpa menambah maklumat tentang pengguna yang menerima mesej.

## Common Examples

### Menghantar mesej ringkas
Untuk menghantar mesej ringkas kepada semua pengguna, anda boleh menggunakan:

```bash
wall "Sistem akan ditutup dalam 10 minit."
```

### Menghantar mesej dari fail
Jika anda mempunyai mesej yang disimpan dalam fail, anda boleh menghantarnya dengan cara berikut:

```bash
wall < /path/to/file.txt
```

### Menghantar mesej tanpa maklumat pengguna
Untuk menghantar mesej tanpa menunjukkan maklumat pengguna, gunakan pilihan `-s`:

```bash
wall -s "Penyelenggaraan sistem akan dijalankan malam ini."
```

## Tips
- Pastikan mesej yang dihantar adalah jelas dan ringkas agar semua pengguna dapat memahami dengan cepat.
- Gunakan `wall` dengan bijak, terutamanya di persekitaran yang mempunyai ramai pengguna, untuk mengelakkan gangguan.
- Sentiasa semak sama ada terdapat pengguna yang aktif sebelum menghantar mesej penting.