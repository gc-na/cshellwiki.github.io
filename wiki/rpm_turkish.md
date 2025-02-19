# [Linux] C Shell (csh) rpm Kullanımı: Paket yönetimi aracı

## Genel Bakış
`rpm` (Red Hat Package Manager), Red Hat tabanlı Linux dağıtımlarında kullanılan bir paket yönetim aracıdır. Yazılım paketlerini kurmak, kaldırmak, güncellemek ve sorgulamak için kullanılır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```
rpm [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-i`: Yeni bir paket kurar.
- `-e`: Mevcut bir paketi kaldırır.
- `-U`: Mevcut bir paketi günceller veya yeni bir paket kurar.
- `-q`: Paket hakkında bilgi sorgular.
- `-l`: Kurulu bir paketin dosyalarını listeler.

## Yaygın Örnekler
Aşağıda `rpm` komutunun bazı yaygın kullanım örnekleri verilmiştir:

### Yeni bir paket kurma
```
rpm -i paket_adı.rpm
```

### Mevcut bir paketi kaldırma
```
rpm -e paket_adı
```

### Mevcut bir paketi güncelleme
```
rpm -U paket_adı.rpm
```

### Kurulu bir paketin bilgilerini sorgulama
```
rpm -q paket_adı
```

### Kurulu bir paketin dosyalarını listeleme
```
rpm -l paket_adı
```

## İpuçları
- Paketlerinizi güncel tutmak için düzenli olarak `rpm -U` komutunu kullanın.
- Hatalı kurulumlar için `--force` seçeneğini kullanarak zorla kurulum yapabilirsiniz, ancak dikkatli olun.
- Paketlerin bağımlılıklarını kontrol etmek için `yum` veya `dnf` gibi araçları kullanmayı düşünün, çünkü `rpm` bağımlılıkları otomatik olarak yönetmez.