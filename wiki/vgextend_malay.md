# [Linux] Bash vgextend Penggunaan: Menambah ruang ke dalam kumpulan volum

## Overview
Perintah `vgextend` digunakan dalam sistem pengurusan storan LVM (Logical Volume Manager) untuk menambah ruang ke dalam kumpulan volum (volume group). Dengan menggunakan perintah ini, anda boleh memperluas kapasiti kumpulan volum dengan menambah satu atau lebih peranti fizikal.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `vgextend`:

```bash
vgextend [options] [volume_group] [physical_device...]
```

## Common Options
- `-f`, `--force`: Memaksa penambahan peranti walaupun terdapat amaran.
- `-n`, `--no-activation`: Menambah peranti tanpa mengaktifkan kumpulan volum.
- `--test`: Melakukan ujian tanpa membuat sebarang perubahan.

## Common Examples
Berikut adalah beberapa contoh penggunaan `vgextend`:

1. Menambah satu peranti fizikal ke dalam kumpulan volum:
   ```bash
   vgextend myvg /dev/sdb1
   ```

2. Menambah beberapa peranti fizikal sekaligus:
   ```bash
   vgextend myvg /dev/sdb1 /dev/sdc1
   ```

3. Menggunakan pilihan `--force` untuk memaksa penambahan:
   ```bash
   vgextend --force myvg /dev/sdd1
   ```

4. Melakukan ujian sebelum menambah peranti:
   ```bash
   vgextend --test myvg /dev/sde1
   ```

## Tips
- Pastikan peranti fizikal yang ingin ditambah sudah tersedia dan tidak digunakan oleh sistem lain.
- Sentiasa lakukan backup data penting sebelum melakukan perubahan pada kumpulan volum.
- Gunakan pilihan `--test` untuk memastikan tiada masalah sebelum melaksanakan perubahan sebenar.