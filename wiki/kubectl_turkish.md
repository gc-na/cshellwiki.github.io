# [Linux] C Shell (csh) kubectl Kullanımı: Kubernetes ile etkileşim kurma

## Genel Bakış
`kubectl`, Kubernetes ile etkileşim kurmak için kullanılan bir komut satırı aracıdır. Kubernetes cluster'ınızı yönetmek, kaynakları kontrol etmek ve uygulama dağıtımlarını yönetmek için çeşitli komutlar sağlar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
kubectl [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `get`: Belirtilen kaynak türlerinin listesini alır.
- `describe`: Belirtilen kaynak hakkında ayrıntılı bilgi verir.
- `apply`: Belirtilen kaynakları oluşturur veya günceller.
- `delete`: Belirtilen kaynakları siler.
- `logs`: Pod'ların günlüklerini görüntüler.

## Yaygın Örnekler
Aşağıda `kubectl` komutunun bazı pratik örnekleri bulunmaktadır:

### Tüm Pod'ları Listeleme
```bash
kubectl get pods
```

### Belirli Bir Pod Hakkında Bilgi Alma
```bash
kubectl describe pod <pod_adı>
```

### Yeni Bir Uygulama Dağıtma
```bash
kubectl apply -f <dosya_adı>.yaml
```

### Bir Pod'u Silme
```bash
kubectl delete pod <pod_adı>
```

### Pod Günlüklerini Görüntüleme
```bash
kubectl logs <pod_adı>
```

## İpuçları
- Komutları daha verimli kullanmak için `--help` seçeneğini kullanarak her komutun yardım metnini görüntüleyebilirsiniz.
- Sık kullandığınız komutları bir alias olarak tanımlayarak zaman kazanabilirsiniz.
- Kubernetes kaynaklarını yönetirken YAML dosyalarını kullanmak, yapılandırmaları daha okunabilir hale getirir.