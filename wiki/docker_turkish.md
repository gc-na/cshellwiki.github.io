# [Linux] Bash docker kullanımı: Docker konteynerlerini yönetme aracı

## Genel Bakış
Docker, uygulamaları konteynerler içinde çalıştırmak için kullanılan bir platformdur. Bu konteynerler, uygulamaların bağımlılıklarıyla birlikte izole bir ortamda çalışmasını sağlar. Docker, geliştiricilere ve sistem yöneticilerine, uygulamaları daha hızlı ve daha güvenilir bir şekilde dağıtma imkanı sunar.

## Kullanım
Docker komutunun temel sözdizimi aşağıdaki gibidir:

```bash
docker [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `run`: Yeni bir konteyner başlatır.
- `ps`: Çalışan konteynerleri listeler.
- `stop`: Çalışan bir konteyneri durdurur.
- `rm`: Bir konteyneri siler.
- `images`: Mevcut Docker imajlarını listeler.

## Yaygın Örnekler
Aşağıda, Docker komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

### Yeni Bir Konteyner Başlatma
```bash
docker run -d --name my_container nginx
```
Bu komut, `nginx` imajından yeni bir konteyner başlatır ve arka planda çalıştırır.

### Çalışan Konteynerleri Listeleme
```bash
docker ps
```
Bu komut, o anda çalışan tüm konteynerleri listeler.

### Bir Konteyneri Durdurma
```bash
docker stop my_container
```
Bu komut, `my_container` adlı konteyneri durdurur.

### Bir Konteyneri Silme
```bash
docker rm my_container
```
Bu komut, durdurulmuş olan `my_container` adlı konteyneri siler.

### Mevcut İmajları Listeleme
```bash
docker images
```
Bu komut, sistemde mevcut olan tüm Docker imajlarını listeler.

## İpuçları
- Konteynerlerinizi yönetirken isimlendirme yaparken anlamlı isimler kullanın, böylece hangi konteynerin ne amaçla kullanıldığını kolayca anlayabilirsiniz.
- Konteynerlerinizi düzenli olarak güncelleyin ve gereksiz olanları silerek sisteminizi temiz tutun.
- Docker komutlarını çalıştırmadan önce `docker --help` komutunu kullanarak mevcut seçenekleri ve argümanları kontrol edin.