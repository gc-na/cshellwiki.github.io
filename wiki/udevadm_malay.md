# [Linux] Bash udevadm Penggunaan: Mengurus peranti dalam sistem Linux

## Overview
Perintah `udevadm` digunakan untuk mengurus dan memantau peranti dalam sistem Linux. Ia berfungsi sebagai antaramuka untuk sistem pengurusan peranti `udev`, yang mengendalikan pengenalan dan pengurusan peranti semasa boot dan semasa operasi sistem.

## Usage
Sintaks asas untuk perintah `udevadm` adalah seperti berikut:

```
udevadm [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk `udevadm` beserta penjelasan ringkas:

- `info`: Menunjukkan maklumat tentang peranti tertentu.
- `trigger`: Memicu pemprosesan peranti oleh `udev`.
- `settle`: Menunggu sehingga semua peranti telah diproses.
- `control`: Mengawal pemprosesan `udev` (contohnya, memulakan atau menghentikan).
- `monitor`: Memantau peristiwa `udev` secara langsung.

## Common Examples

### Menunjukkan maklumat tentang peranti
Untuk mendapatkan maklumat tentang peranti tertentu, anda boleh menggunakan:

```bash
udevadm info --query=all --name=/dev/sda
```

### Memicu pemprosesan peranti
Untuk memicu pemprosesan semua peranti yang tersedia, gunakan:

```bash
udevadm trigger
```

### Menunggu sehingga semua peranti diproses
Jika anda ingin memastikan semua peranti telah diproses, jalankan:

```bash
udevadm settle
```

### Memantau peristiwa `udev`
Untuk memantau peristiwa yang berkaitan dengan peranti secara langsung, gunakan:

```bash
udevadm monitor
```

## Tips
- Sentiasa gunakan `udevadm info` untuk mendapatkan maklumat terperinci tentang peranti sebelum melakukan perubahan.
- Gunakan `udevadm trigger` selepas menambah atau mengubah suai peraturan `udev` untuk memastikan perubahan tersebut berkuat kuasa.
- Pastikan anda menjalankan perintah ini dengan hak akses yang sesuai, terutamanya jika melibatkan perubahan pada peranti sistem.