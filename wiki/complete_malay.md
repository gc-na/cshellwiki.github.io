# [Linux] Bash lengkap penggunaan: Melengkapkan arahan

## Overview
Arahan `complete` dalam Bash digunakan untuk mengkonfigurasi dan mengawal cara pelengkap automatik berfungsi untuk arahan tertentu. Ini membolehkan pengguna untuk menambah atau mengubah suai pilihan pelengkap yang tersedia semasa menaip arahan di terminal.

## Usage
Sintaks asas untuk arahan `complete` adalah seperti berikut:

```bash
complete [options] [arguments]
```

## Common Options
- `-A`: Menentukan jenis argumen yang akan dilengkapkan, seperti `command`, `file`, atau `directory`.
- `-o`: Menambah pilihan pelengkap tertentu, seperti `default` atau `nospace`.
- `-F`: Menggunakan fungsi pelengkap yang ditentukan untuk melengkapkan argumen.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `complete`:

1. **Melengkapkan nama fail untuk arahan `cp`:**
   ```bash
   complete -o nospace -F _filedir cp
   ```

2. **Menambah pelengkap untuk arahan `git`:**
   ```bash
   complete -o default -F _git git
   ```

3. **Menggunakan pelengkap untuk arahan `ssh`:**
   ```bash
   complete -A host -o nospace ssh
   ```

4. **Menambah pelengkap untuk arahan `mycommand`:**
   ```bash
   complete -W "option1 option2 option3" mycommand
   ```

## Tips
- Sentiasa semak pelengkap yang sudah ada sebelum menambah yang baru untuk mengelakkan konflik.
- Gunakan fungsi pelengkap untuk pelengkap yang lebih kompleks dan dinamik.
- Uji pelengkap baru anda di terminal sebelum menyimpannya dalam fail konfigurasi seperti `.bashrc` untuk memastikan ia berfungsi seperti yang diharapkan.