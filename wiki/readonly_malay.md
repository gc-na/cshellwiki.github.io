# [Linux] Bash readonly Penggunaan: Menetapkan Pembolehubah Hanya Baca

## Overview
Perintah `readonly` dalam Bash digunakan untuk menetapkan pembolehubah sebagai hanya baca. Ini bermakna setelah pembolehubah ditetapkan sebagai `readonly`, nilainya tidak boleh diubah atau dipadam dalam sesi shell yang sama.

## Usage
Sintaks asas untuk menggunakan perintah `readonly` adalah seperti berikut:

```bash
readonly [options] [arguments]
```

## Common Options
- `-p`: Menunjukkan semua pembolehubah yang ditetapkan sebagai `readonly` dalam sesi semasa.

## Common Examples

### Menetapkan Pembolehubah Sebagai Hanya Baca
Untuk menetapkan pembolehubah `VAR1` sebagai hanya baca, gunakan perintah berikut:

```bash
readonly VAR1="Hello World"
```

### Mencuba Mengubah Nilai Pembolehubah
Setelah menetapkan `VAR1` sebagai `readonly`, jika anda cuba mengubah nilainya, anda akan mendapat ralat:

```bash
VAR1="New Value"  # Ini akan menghasilkan ralat
```

### Menunjukkan Pembolehubah Hanya Baca
Untuk melihat semua pembolehubah yang ditetapkan sebagai `readonly`, gunakan:

```bash
readonly -p
```

## Tips
- Gunakan `readonly` untuk melindungi pembolehubah penting dalam skrip anda daripada diubah secara tidak sengaja.
- Sentiasa semak senarai pembolehubah `readonly` sebelum menetapkan yang baru untuk mengelakkan konflik.
- Pembolehubah yang ditetapkan sebagai `readonly` hanya terpakai dalam sesi shell semasa; mereka tidak akan kekal selepas sesi ditutup.