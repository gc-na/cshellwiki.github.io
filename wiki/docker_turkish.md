# [Linux] C Shell (csh) docker kullanımı: Docker konteynerlerini yönetme

## Genel Bakış
Docker, yazılım uygulamalarını konteynerler içinde paketlemek, dağıtmak ve çalıştırmak için kullanılan bir platformdur. Bu, uygulamaların bağımlılıklarıyla birlikte taşınabilir ve izole bir ortamda çalışmasını sağlar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```csh
docker [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `run`: Yeni bir konteyner başlatır.
- `ps`: Çalışan konteynerlerin listesini gösterir.
- `stop`: Çalışan bir konteyneri durdurur.
- `rm`: Bir konteyneri siler.
- `images`: Mevcut Docker imajlarını listeler.

## Yaygın Örnekler
Aşağıda, Docker komutlarının bazı pratik örnekleri verilmiştir:

### Yeni Bir Konteyner Başlatma
```csh
docker run -d --name my_container nginx
```
Bu komut, `nginx` imajını kullanarak arka planda (`-d` seçeneği ile) `my_container` adında yeni bir konteyner başlatır.

### Çalışan Konteynerleri Listeleme
```csh
docker ps
```
Bu komut, o anda çalışan tüm konteynerlerin listesini gösterir.

### Konteyneri Durdurma
```csh
docker stop my_container
```
Bu komut, `my_container` adındaki konteyneri durdurur.

### Konteyneri Silme
```csh
docker rm my_container
```
Bu komut, durdurulmuş olan `my_container` adındaki konteyneri siler.

### Mevcut İmajları Listeleme
```csh
docker images
```
Bu komut, sistemde mevcut olan tüm Docker imajlarını listeler.

## İpuçları
- Konteynerlerinizi yönetirken isimlendirme kurallarına dikkat edin; bu, takip etmeyi kolaylaştırır.
- Konteynerlerinizi düzenli olarak güncelleyin ve gereksiz olanları silin.
- Docker imajlarınızı optimize edin; bu, daha hızlı dağıtım ve daha az disk alanı kullanımı sağlar.