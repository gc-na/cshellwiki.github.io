# [Linux] Bash popd Penggunaan: Menghapus direktori dari tumpukan

## Overview
Perintah `popd` digunakan dalam Bash untuk menghapus direktori dari tumpukan direktori yang telah disimpan sebelumnya dengan perintah `pushd`. Ini memungkinkan pengguna untuk dengan mudah berpindah kembali ke direktori yang sebelumnya telah diakses.

## Usage
Berikut adalah sintaks dasar dari perintah `popd`:

```
popd [options] [arguments]
```

## Common Options
- `-n`: Menjalankan perintah tanpa mengubah direktori saat ini.
- `+n`: Menghapus direktori dari tumpukan berdasarkan indeks, di mana `n` adalah indeks yang dimulai dari 0.
- `-n`: Menghapus direktori dari tumpukan dengan menghitung dari belakang.

## Common Examples
Berikut adalah beberapa contoh penggunaan `popd`:

1. **Menghapus direktori teratas dari tumpukan:**
   ```bash
   pushd /home/user/Documents
   pushd /home/user/Downloads
   popd
   ```
   Dalam contoh ini, `popd` akan menghapus `/home/user/Downloads` dari tumpukan dan kembali ke `/home/user/Documents`.

2. **Menghapus direktori tertentu dari tumpukan menggunakan indeks:**
   ```bash
   pushd /home/user/Documents
   pushd /home/user/Downloads
   pushd /home/user/Pictures
   popd +1
   ```
   Di sini, `popd +1` akan menghapus `/home/user/Downloads` dari tumpukan, dan direktori yang aktif akan menjadi `/home/user/Documents`.

3. **Menggunakan opsi -n untuk tidak mengubah direktori saat ini:**
   ```bash
   pushd /home/user/Documents
   pushd /home/user/Downloads
   popd -n
   ```
   Dengan menggunakan `popd -n`, direktori saat ini tetap di `/home/user/Downloads`, tetapi `/home/user/Documents` tetap ada di tumpukan.

## Tips
- Selalu gunakan `pushd` sebelum `popd` untuk memastikan tumpukan direktori berfungsi dengan baik.
- Gunakan `dirs` untuk melihat isi tumpukan direktori saat ini sebelum menggunakan `popd`.
- Ingat bahwa indeks dimulai dari 0, jadi `+1` akan mengacu pada direktori kedua dalam tumpukan.