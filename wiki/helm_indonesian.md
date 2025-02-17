# [Linux] Bash helm penggunaan: Mengelola paket aplikasi Kubernetes

## Overview
Perintah `helm` adalah alat manajemen paket untuk Kubernetes yang memungkinkan pengguna untuk menginstal, mengelola, dan menghapus aplikasi dalam bentuk chart. Helm memudahkan proses penyebaran aplikasi dengan menyediakan cara untuk mengelola konfigurasi dan dependensi.

## Usage
Berikut adalah sintaks dasar untuk perintah helm:

```bash
helm [options] [arguments]
```

## Common Options
- `install`: Menginstal chart ke dalam cluster Kubernetes.
- `upgrade`: Memperbarui rilis chart yang sudah ada.
- `uninstall`: Menghapus rilis chart dari cluster.
- `list`: Menampilkan daftar rilis chart yang terinstal.
- `repo`: Mengelola repositori chart.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah helm:

### Menginstal Chart
Untuk menginstal chart, gunakan perintah berikut:

```bash
helm install my-release stable/nginx
```

### Memperbarui Rilis
Untuk memperbarui rilis yang sudah ada, gunakan:

```bash
helm upgrade my-release stable/nginx
```

### Menghapus Rilis
Untuk menghapus rilis dari cluster, gunakan:

```bash
helm uninstall my-release
```

### Menampilkan Daftar Rilis
Untuk melihat daftar rilis yang terinstal, gunakan:

```bash
helm list
```

### Mengelola Repositori Chart
Untuk menambahkan repositori chart, gunakan:

```bash
helm repo add my-repo https://example.com/charts
```

## Tips
- Selalu periksa versi chart sebelum menginstal atau memperbarui untuk memastikan kompatibilitas.
- Gunakan `helm search` untuk menemukan chart yang tersedia di repositori.
- Simpan konfigurasi chart dalam file YAML untuk memudahkan pengelolaan dan pemeliharaan.