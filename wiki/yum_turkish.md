# [Linux] C Shell (csh) yum Kullanımı: Paket yönetimi aracı

## Genel Bakış
`yum`, Red Hat tabanlı Linux dağıtımlarında kullanılan bir paket yönetim aracıdır. Kullanıcıların yazılım paketlerini yüklemesine, güncellemesine ve kaldırmasına olanak tanır. `yum`, bağımlılıkları otomatik olarak yönetir ve sistemin güncel kalmasını sağlar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```
yum [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `install`: Belirtilen paketi yükler.
- `remove`: Belirtilen paketi kaldırır.
- `update`: Yüklü paketleri günceller.
- `list`: Mevcut paketleri listeler.
- `search`: Belirtilen terimi içeren paketleri arar.

## Yaygın Örnekler
Aşağıda `yum` komutunun bazı pratik örnekleri bulunmaktadır:

### 1. Paket Yükleme
Belirli bir paketi yüklemek için:
```bash
yum install paket_adi
```

### 2. Paket Kaldırma
Belirli bir paketi kaldırmak için:
```bash
yum remove paket_adi
```

### 3. Paket Güncelleme
Tüm yüklü paketleri güncellemek için:
```bash
yum update
```

### 4. Paket Arama
Belirli bir terimi içeren paketleri aramak için:
```bash
yum search arama_terimi
```

### 5. Mevcut Paketleri Listeleme
Tüm mevcut paketleri listelemek için:
```bash
yum list
```

## İpuçları
- `yum` komutunu çalıştırmadan önce, sisteminizin güncel olduğundan emin olun.
- Paket yüklemeden önce, hangi bağımlılıkların yükleneceğini kontrol edin.
- `yum clean all` komutunu kullanarak önbelleği temizleyebilirsiniz; bu, disk alanı tasarrufu sağlar.
- `yum info paket_adi` komutuyla bir paketin detaylarını görüntüleyebilirsiniz.