# [Linux] Bash helm penggunaan: Mengurus aplikasi Kubernetes

## Overview
Perintah `helm` adalah pengurus pakej untuk Kubernetes yang membolehkan pengguna untuk mengurus aplikasi yang berjalan di dalam kluster Kubernetes. Ia memudahkan proses pemasangan, pengemaskinian, dan penghapusan aplikasi dengan menggunakan "chart", yang merupakan koleksi fail yang menggambarkan sumber yang diperlukan oleh aplikasi.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah helm:

```bash
helm [options] [arguments]
```

## Common Options
- `install`: Memasang chart baru ke dalam kluster.
- `upgrade`: Mengemas kini chart yang sudah dipasang.
- `uninstall`: Menghapus chart dari kluster.
- `list`: Menyenaraikan semua releas yang telah dipasang.
- `repo`: Mengurus repositori chart.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan helm:

### Memasang Chart
Untuk memasang chart baru, gunakan perintah berikut:

```bash
helm install my-release stable/mysql
```

### Mengemas Kini Chart
Untuk mengemas kini releas yang telah dipasang:

```bash
helm upgrade my-release stable/mysql
```

### Menghapus Chart
Untuk menghapus releas dari kluster:

```bash
helm uninstall my-release
```

### Menyenaraikan Releas
Untuk melihat semua releas yang telah dipasang:

```bash
helm list
```

### Mengurus Repositori Chart
Untuk menambah repositori chart baru:

```bash
helm repo add my-repo https://charts.example.com
```

## Tips
- Sentiasa periksa versi chart yang tersedia sebelum memasang untuk memastikan anda menggunakan versi yang stabil.
- Gunakan `helm template` untuk merender chart ke dalam fail YAML sebelum pemasangan untuk memeriksa konfigurasi.
- Simpan konfigurasi chart dalam sistem kawalan versi untuk memudahkan pengurusan dan pengulangan pemasangan.