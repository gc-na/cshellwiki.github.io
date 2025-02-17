# [Linux] Bash minikube Penggunaan: Mengelola kluster Kubernetes lokal

## Overview
Minikube adalah alat yang memungkinkan pengguna untuk menjalankan kluster Kubernetes lokal di mesin mereka. Dengan minikube, Anda dapat dengan mudah mengembangkan dan menguji aplikasi yang berjalan di Kubernetes tanpa memerlukan infrastruktur cloud yang kompleks.

## Usage
Berikut adalah sintaks dasar dari perintah minikube:

```
minikube [options] [arguments]
```

## Common Options
- `start`: Memulai kluster minikube baru.
- `stop`: Menghentikan kluster minikube yang sedang berjalan.
- `status`: Menampilkan status dari kluster minikube.
- `delete`: Menghapus kluster minikube yang sudah ada.
- `dashboard`: Membuka dashboard Kubernetes di browser.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah minikube:

1. **Memulai kluster minikube baru:**
   ```bash
   minikube start
   ```

2. **Menghentikan kluster yang sedang berjalan:**
   ```bash
   minikube stop
   ```

3. **Menampilkan status kluster:**
   ```bash
   minikube status
   ```

4. **Menghapus kluster minikube:**
   ```bash
   minikube delete
   ```

5. **Membuka dashboard Kubernetes:**
   ```bash
   minikube dashboard
   ```

## Tips
- Pastikan Anda memiliki virtualisasi yang diaktifkan di BIOS untuk menjalankan minikube dengan lancar.
- Gunakan `minikube config` untuk mengatur konfigurasi default seperti driver dan jumlah CPU.
- Selalu periksa versi minikube Anda dengan `minikube version` untuk memastikan Anda menggunakan versi terbaru.