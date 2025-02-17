# [Linux] Bash helm kullanımı: Helm, Kubernetes uygulamalarını yönetmek için bir paket yöneticisidir.

## Overview
Helm, Kubernetes üzerinde uygulamaları yönetmek için kullanılan bir paket yöneticisidir. Helm, uygulamaların dağıtımını, güncellenmesini ve yönetimini kolaylaştırır. Helm ile uygulama paketleri "chart" adı verilen yapılandırma dosyaları olarak tanımlanır.

## Usage
Helm komutunun temel sözdizimi aşağıdaki gibidir:

```bash
helm [options] [arguments]
```

## Common Options
- `install`: Bir chart'ı yüklemek için kullanılır.
- `upgrade`: Mevcut bir release'i güncellemek için kullanılır.
- `uninstall`: Bir release'i kaldırmak için kullanılır.
- `list`: Yüklenmiş olan release'lerin listesini gösterir.
- `repo`: Helm repository'lerini yönetmek için kullanılır.

## Common Examples
Aşağıda helm komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. **Chart Yüklemek:**
   ```bash
   helm install my-release my-chart
   ```

2. **Release Güncellemek:**
   ```bash
   helm upgrade my-release my-chart
   ```

3. **Release Kaldırmak:**
   ```bash
   helm uninstall my-release
   ```

4. **Yüklenmiş Release'leri Listelemek:**
   ```bash
   helm list
   ```

5. **Repository Ekleme:**
   ```bash
   helm repo add my-repo https://example.com/charts
   ```

## Tips
- Helm chart'larınızı versiyon kontrolü altında tutmak, güncellemeleri yönetmeyi kolaylaştırır.
- Helm komutlarını çalıştırmadan önce `helm repo update` komutunu kullanarak repository'lerinizi güncel tutun.
- Uygulama dağıtımında rollback (geri alma) işlemleri için `helm rollback` komutunu kullanmayı unutmayın.