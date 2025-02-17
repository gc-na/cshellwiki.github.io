# [Linux] Bash mesg Penggunaan: Mengawal mesej sistem

## Overview
Perintah `mesg` digunakan dalam Bash untuk mengawal sama ada pengguna lain boleh menghantar mesej ke terminal anda. Ia membolehkan anda mengawal privasi dan gangguan semasa bekerja di sistem.

## Usage
Sintaks asas untuk perintah `mesg` adalah seperti berikut:

```bash
mesg [options] [arguments]
```

## Common Options
- `y` : Benarkan pengguna lain menghantar mesej ke terminal anda.
- `n` : Larang pengguna lain daripada menghantar mesej ke terminal anda.
- `--help` : Paparkan bantuan tentang penggunaan perintah ini.

## Common Examples
1. **Benarkan mesej dari pengguna lain:**
   ```bash
   mesg y
   ```

2. **Larangkan mesej dari pengguna lain:**
   ```bash
   mesg n
   ```

3. **Dapatkan bantuan mengenai perintah mesg:**
   ```bash
   mesg --help
   ```

## Tips
- Gunakan `mesg n` apabila anda memerlukan fokus dan tidak mahu terganggu oleh mesej dari pengguna lain.
- Sebelum menjalankan perintah `mesg y`, pastikan anda bersedia untuk menerima mesej, terutamanya jika anda berada dalam persekitaran kerja yang sibuk.
- Perintah ini hanya berfungsi dalam sesi terminal yang sama dan tidak akan mempengaruhi sesi lain yang sedang berjalan.