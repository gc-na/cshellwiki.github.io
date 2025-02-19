# [Sistem Operasi] C Shell (csh) renice: Mengubah prioritas proses

## Overview
Perintah `renice` digunakan untuk mengubah prioritas dari proses yang sedang berjalan di sistem. Dengan mengubah prioritas ini, pengguna dapat menentukan seberapa banyak sumber daya CPU yang akan dialokasikan untuk proses tertentu, yang dapat membantu dalam pengelolaan beban kerja sistem.

## Usage
Berikut adalah sintaks dasar dari perintah `renice`:

```csh
renice [options] [arguments]
```

## Common Options
- `-n`: Menentukan nilai prioritas baru. Nilai ini dapat berupa angka negatif (untuk meningkatkan prioritas) atau angka positif (untuk menurunkan prioritas).
- `-p`: Menggunakan ID proses (PID) untuk menentukan proses yang ingin diubah prioritasnya.
- `-g`: Menggunakan ID grup proses untuk mengubah prioritas semua proses dalam grup tersebut.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `renice`:

1. Mengubah prioritas proses dengan PID 1234 menjadi 10:
    ```csh
    renice -n 10 -p 1234
    ```

2. Meningkatkan prioritas proses dengan PID 5678 menjadi -5:
    ```csh
    renice -n -5 -p 5678
    ```

3. Mengubah prioritas semua proses dalam grup dengan ID grup 1000 menjadi 15:
    ```csh
    renice -n 15 -g 1000
    ```

4. Menurunkan prioritas proses dengan PID 4321 menjadi 19:
    ```csh
    renice -n 19 -p 4321
    ```

## Tips
- Selalu periksa prioritas proses sebelum mengubahnya dengan menggunakan perintah `ps` untuk memastikan bahwa perubahan yang dilakukan sesuai dengan kebutuhan.
- Hati-hati saat meningkatkan prioritas proses, karena dapat menyebabkan proses lain menjadi lambat atau tidak responsif.
- Gunakan nilai prioritas negatif dengan bijaksana, karena dapat mengakibatkan penggunaan CPU yang tinggi oleh proses yang diprioritaskan.