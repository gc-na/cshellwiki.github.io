# [Linux] Bash yum Kullanımı: Paket yönetimi aracı

## Genel Bakış
`yum`, Red Hat tabanlı Linux dağıtımlarında kullanılan bir paket yönetim aracıdır. Kullanıcıların yazılım paketlerini yüklemesine, güncellemesine ve kaldırmasına olanak tanır. Ayrıca, bağımlılıkları otomatik olarak yönetir ve sistemin güncel kalmasını sağlar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
yum [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `install`: Belirtilen paketi yükler.
- `remove`: Belirtilen paketi kaldırır.
- `update`: Yüklü paketleri günceller.
- `search`: Belirtilen terime göre paket arar.
- `info`: Belirtilen paket hakkında bilgi verir.

## Yaygın Örnekler
Aşağıda `yum` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

### 1. Bir Paketi Yüklemek
```bash
yum install httpd
```
Bu komut, Apache web sunucusunu yükler.

### 2. Bir Paketi Kaldırmak
```bash
yum remove httpd
```
Bu komut, Apache web sunucusunu sistemden kaldırır.

### 3. Tüm Paketleri Güncellemek
```bash
yum update
```
Bu komut, sistemdeki tüm yüklü paketleri günceller.

### 4. Bir Paketi Aramak
```bash
yum search vim
```
Bu komut, `vim` metin düzenleyicisini içeren paketleri arar.

### 5. Bir Paketin Bilgilerini Görüntülemek
```bash
yum info httpd
```
Bu komut, Apache web sunucusu hakkında detaylı bilgi verir.

## İpuçları
- `yum` komutunu kullanmadan önce sisteminizin güncel olduğundan emin olun.
- Paket yükleme veya kaldırma işlemlerinden önce, işlem yapacağınız paketin bağımlılıklarını kontrol edin.
- `yum clean all` komutunu kullanarak önbelleği temizlemek, sistemin daha verimli çalışmasına yardımcı olabilir.