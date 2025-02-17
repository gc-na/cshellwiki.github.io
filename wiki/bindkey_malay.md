# [Linux] Bash bindkey Penggunaan: Mengikat kekunci untuk fungsi tertentu

## Overview
Perintah `bindkey` digunakan dalam shell seperti zsh untuk mengikat kekunci tertentu kepada fungsi atau perintah. Ini membolehkan pengguna untuk mempercepatkan kerja mereka dengan menetapkan kekunci pintasan yang sesuai dengan keperluan mereka.

## Usage
Berikut adalah sintaks asas untuk perintah `bindkey`:

```bash
bindkey [options] [arguments]
```

## Common Options
- `-e` : Menggunakan mod emacs untuk kekunci.
- `-v` : Menggunakan mod vi untuk kekunci.
- `-s` : Mengikat kekunci untuk memasukkan teks secara langsung.
- `-l` : Menunjukkan semua kekunci yang telah diikat.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `bindkey`:

### Mengikat kekunci untuk perintah tertentu
Mengikat kekunci `Ctrl + x` untuk menjalankan perintah `ls`:

```bash
bindkey '^X' 'ls\n'
```

### Mengubah kekunci untuk fungsi navigasi
Mengikat kekunci `Alt + b` untuk bergerak ke belakang satu perkataan:

```bash
bindkey 'M-b' backward-word
```

### Menggunakan mod vi
Mengaktifkan mod vi untuk kekunci:

```bash
bindkey -v
```

### Menunjukkan semua kekunci yang diikat
Menunjukkan semua kekunci yang telah diikat dalam sesi semasa:

```bash
bindkey -l
```

## Tips
- Pastikan untuk menyimpan pengikatan kekunci dalam fail konfigurasi shell anda untuk penggunaan yang berterusan.
- Gunakan `bindkey -L` untuk melihat senarai semua pengikatan kekunci yang ada.
- Eksperimen dengan pengikatan kekunci untuk meningkatkan produktiviti anda dalam terminal.