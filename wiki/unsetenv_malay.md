# [Linux] Bash unsetenv Penggunaan: Menghapus pembolehubah persekitaran

## Overview
Perintah `unsetenv` digunakan untuk menghapus pembolehubah persekitaran dalam sesi terminal. Dengan menggunakan perintah ini, anda boleh menghapuskan pembolehubah yang tidak lagi diperlukan, membantu mengekalkan kebersihan dan organisasi dalam persekitaran kerja anda.

## Usage
Berikut adalah sintaks asas untuk perintah `unsetenv`:

```bash
unsetenv [options] [arguments]
```

## Common Options
- Tiada pilihan khusus untuk `unsetenv`, tetapi anda boleh menggunakannya dengan pembolehubah yang ingin dihapuskan.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `unsetenv`:

1. **Menghapuskan satu pembolehubah persekitaran:**

```bash
unsetenv MY_VARIABLE
```

2. **Menghapuskan beberapa pembolehubah persekitaran sekaligus:**

```bash
unsetenv VAR1 VAR2 VAR3
```

3. **Menghapuskan pembolehubah persekitaran dalam skrip:**

```bash
#!/bin/bash
unsetenv TEMP_VAR
echo "TEMP_VAR telah dihapuskan."
```

## Tips
- Pastikan anda tahu pembolehubah yang ingin dihapuskan sebelum menggunakan `unsetenv`, kerana tindakan ini tidak boleh dibatalkan.
- Gunakan `printenv` atau `env` untuk menyemak senarai pembolehubah persekitaran yang ada sebelum menghapuskan.
- Jika anda menggunakan `unsetenv` dalam skrip, pertimbangkan untuk menambah komen untuk menjelaskan mengapa pembolehubah tersebut dihapuskan.