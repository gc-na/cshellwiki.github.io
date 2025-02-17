# [Linux] Bash mkfs Penggunaan: Membuat sistem fail pada peranti storan

## Overview
Perintah `mkfs` (make filesystem) digunakan untuk membuat sistem fail pada peranti storan seperti cakera keras, pemacu USB, atau partisi. Ia memformat peranti tersebut dengan sistem fail yang ditentukan, membolehkan data disimpan dan diuruskan dengan berkesan.

## Usage
Sintaks asas bagi perintah `mkfs` adalah seperti berikut:

```bash
mkfs [options] [arguments]
```

## Common Options
- `-t, --type`: Menentukan jenis sistem fail yang ingin digunakan (contohnya, ext4, vfat).
- `-L, --label`: Memberikan label kepada sistem fail yang sedang dibuat.
- `-V, --verbose`: Mengaktifkan mod verbose untuk menunjukkan lebih banyak maklumat semasa proses.
- `-n, --no-magic`: Mengelakkan penulisan "magic number" pada sistem fail.

## Common Examples
Berikut adalah beberapa contoh penggunaan `mkfs`:

1. Membuat sistem fail ext4 pada peranti `/dev/sdb1`:
   ```bash
   mkfs -t ext4 /dev/sdb1
   ```

2. Membuat sistem fail FAT32 dan memberikan label "USB_DRIVE":
   ```bash
   mkfs -t vfat -L USB_DRIVE /dev/sdc1
   ```

3. Menggunakan mod verbose semasa memformat:
   ```bash
   mkfs -V -t ext3 /dev/sdd1
   ```

4. Membuat sistem fail dengan tanpa menulis "magic number":
   ```bash
   mkfs -n -t ext4 /dev/sde1
   ```

## Tips
- Pastikan anda telah membuat salinan sandaran data penting sebelum menggunakan `mkfs`, kerana proses ini akan memadam semua data pada peranti yang diformat.
- Gunakan pilihan `-L` untuk memberikan label yang mudah dikenali bagi sistem fail anda, memudahkan pengurusan.
- Sentiasa semak peranti yang ingin diformat dengan menggunakan perintah `lsblk` atau `fdisk -l` untuk mengelakkan kesilapan.