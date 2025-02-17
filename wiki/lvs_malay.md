# [Linux] Bash lvs Penggunaan: Menunjukkan maklumat tentang Logical Volumes

## Overview
Perintah `lvs` digunakan dalam sistem pengendalian Linux untuk memaparkan maklumat mengenai Logical Volumes (LV) dalam Logical Volume Management (LVM). Ia memberikan pandangan ringkas tentang semua LV yang ada, termasuk saiz, status, dan atribut lain.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `lvs`:

```bash
lvs [options] [arguments]
```

## Common Options
- `-a` : Menunjukkan semua logical volumes termasuk yang tidak aktif.
- `-o` : Memilih kolum tertentu untuk dipaparkan.
- `-n` : Menunjukkan nama logical volume.
- `-r` : Menunjukkan maklumat dalam format ringkas.
- `--units` : Menentukan unit yang digunakan untuk memaparkan saiz.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `lvs`:

1. **Paparkan semua logical volumes:**
   ```bash
   lvs
   ```

2. **Paparkan semua logical volumes termasuk yang tidak aktif:**
   ```bash
   lvs -a
   ```

3. **Paparkan maklumat tertentu tentang logical volumes:**
   ```bash
   lvs -o +devices
   ```

4. **Paparkan nama logical volume:**
   ```bash
   lvs -n
   ```

5. **Paparkan maklumat dalam format ringkas:**
   ```bash
   lvs -r
   ```

## Tips
- Sentiasa gunakan pilihan `-o` untuk menyesuaikan maklumat yang dipaparkan mengikut keperluan anda.
- Gunakan `lvs --units m` untuk memaparkan saiz dalam megabait, menjadikannya lebih mudah dibaca.
- Untuk maklumat lebih terperinci, pertimbangkan untuk menggunakan perintah `lvdisplay` bersamaan dengan `lvs`.