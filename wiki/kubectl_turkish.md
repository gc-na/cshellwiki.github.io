# [Linux] Bash kubectl Kullanımı: Kubernetes kaynaklarını yönetmek için bir komut

## Genel Bakış
`kubectl`, Kubernetes kümesindeki kaynakları yönetmek için kullanılan bir komuttur. Bu komut, pod'lar, hizmetler, dağıtımlar ve diğer Kubernetes bileşenleri üzerinde işlemler yapmanıza olanak tanır. `kubectl`, kullanıcıların Kubernetes ile etkileşimde bulunmasını sağlayarak uygulama dağıtımını ve yönetimini kolaylaştırır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
kubectl [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `get`: Belirtilen kaynak türlerini listelemek için kullanılır.
- `describe`: Belirtilen kaynak hakkında daha ayrıntılı bilgi almak için kullanılır.
- `create`: Yeni bir kaynak oluşturmak için kullanılır.
- `delete`: Belirtilen bir kaynağı silmek için kullanılır.
- `apply`: Bir kaynak üzerinde değişiklik yapmak için kullanılır.

## Yaygın Örnekler
- Tüm pod'ları listelemek için:
```bash
kubectl get pods
```

- Belirli bir pod hakkında ayrıntılı bilgi almak için:
```bash
kubectl describe pod <pod_adı>
```

- Yeni bir dağıtım oluşturmak için:
```bash
kubectl create deployment <dağıtım_adı> --image=<görüntü_adı>
```

- Belirli bir kaynağı silmek için:
```bash
kubectl delete pod <pod_adı>
```

- Uygulama yapılandırmalarını güncellemek için:
```bash
kubectl apply -f <dosya_adı>.yaml
```

## İpuçları
- `kubectl` komutlarını daha verimli kullanmak için, sık kullandığınız komutları bir alias olarak tanımlayabilirsiniz.
- Kubernetes kaynaklarının durumunu kontrol etmek için `kubectl get` komutunu düzenli olarak kullanın.
- YAML dosyaları ile çalışırken, dosya yapısına dikkat edin; doğru girintiler ve formatlama, komutların doğru çalışmasını sağlar.