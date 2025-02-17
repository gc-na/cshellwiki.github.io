# [Linux] Bash vgcreate Penggunaan: Mencipta kumpulan volum

## Overview
Perintah `vgcreate` digunakan dalam sistem pengurusan storan LVM (Logical Volume Manager) untuk mencipta kumpulan volum baru. Kumpulan volum adalah satu set daripada satu atau lebih peranti blok yang boleh digunakan untuk mengurus ruang storan dengan lebih fleksibel.

## Usage
Sintaks asas untuk perintah `vgcreate` adalah seperti berikut:

```bash
vgcreate [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk `vgcreate` beserta penjelasan ringkas:

- `-n, --name <name>`: Menetapkan nama untuk kumpulan volum yang baru.
- `-s, --stripes <stripes>`: Menentukan bilangan jalur untuk kumpulan volum.
- `-p, --maxlogicalvolumes <number>`: Menetapkan jumlah maksimum volum logik yang boleh dicipta dalam kumpulan volum.
- `-f, --force`: Memaksa penciptaan kumpulan volum walaupun terdapat amaran.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `vgcreate`:

1. **Mencipta kumpulan volum baru dengan nama "vg01":**

    ```bash
    vgcreate vg01 /dev/sdb1 /dev/sdc1
    ```

2. **Mencipta kumpulan volum dengan nama "vg_data" dan menetapkan bilangan jalur:**

    ```bash
    vgcreate -n vg_data -s 64k vg_data /dev/sdb1
    ```

3. **Mencipta kumpulan volum dengan memaksa penciptaan walaupun terdapat amaran:**

    ```bash
    vgcreate -f vg01 /dev/sdb1
    ```

## Tips
- Pastikan peranti blok yang ingin digunakan tidak sedang digunakan oleh sistem lain sebelum mencipta kumpulan volum.
- Sentiasa semak status kumpulan volum menggunakan perintah `vgs` selepas penciptaan untuk memastikan ia telah dicipta dengan betul.
- Gunakan pilihan `-f` dengan berhati-hati, kerana ia boleh mengabaikan amaran penting yang mungkin menyebabkan kehilangan data.