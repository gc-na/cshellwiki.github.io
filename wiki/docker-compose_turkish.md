# [Linux] C Shell (csh) docker-compose Kullanımı: Docker konteynerlerini yönetmek için bir araç

## Genel Bakış
`docker-compose`, birden fazla Docker konteynerini tanımlamak ve yönetmek için kullanılan bir araçtır. Kullanıcıların birden fazla hizmeti tek bir yapılandırma dosyası ile kolayca başlatmalarına, durdurmalarına ve yönetmelerine olanak tanır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
docker-compose [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `up`: Tanımlı hizmetleri başlatır.
- `down`: Başlatılan hizmetleri durdurur ve ağları temizler.
- `build`: Hizmetler için Docker imajlarını oluşturur.
- `logs`: Hizmetlerin günlüklerini görüntüler.
- `ps`: Çalışan hizmetlerin durumunu listeler.

## Yaygın Örnekler
Aşağıda `docker-compose` komutunun bazı pratik örnekleri bulunmaktadır:

### Hizmetleri Başlatma
```bash
docker-compose up
```
Bu komut, `docker-compose.yml` dosyasında tanımlı olan tüm hizmetleri başlatır.

### Hizmetleri Durdurma
```bash
docker-compose down
```
Bu komut, başlatılan tüm hizmetleri durdurur ve kaynakları temizler.

### İmajları Oluşturma
```bash
docker-compose build
```
Bu komut, tanımlı hizmetler için gerekli Docker imajlarını oluşturur.

### Günlükleri Görüntüleme
```bash
docker-compose logs
```
Bu komut, başlatılan hizmetlerin günlüklerini görüntüler.

### Çalışan Hizmetlerin Durumunu Listeleme
```bash
docker-compose ps
```
Bu komut, mevcut çalışan hizmetlerin durumunu gösterir.

## İpuçları
- `docker-compose up -d`: Hizmetleri arka planda çalıştırmak için `-d` seçeneğini kullanabilirsiniz.
- `docker-compose exec <hizmet> <komut>`: Çalışan bir hizmet içinde komut çalıştırmak için bu komutu kullanın.
- Yapılandırma dosyanızı düzenli tutun ve yorumlar ekleyerek açıklamalar yapın, böylece ekip arkadaşlarınız için daha anlaşılır hale gelir.