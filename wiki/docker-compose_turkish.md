# [Linux] Bash docker-compose Kullanımı: Docker konteynerlerini yönetmek için bir araç

## Overview
`docker-compose`, birden fazla Docker konteynerini tanımlamak ve yönetmek için kullanılan bir araçtır. Kullanıcıların uygulama bileşenlerini bir araya getirerek, tek bir komutla tüm hizmetleri başlatmalarına, durdurmalarına veya güncellemelerine olanak tanır.

## Usage
Temel kullanım sözdizimi aşağıdaki gibidir:

```bash
docker-compose [options] [arguments]
```

## Common Options
- `up`: Tanımlı hizmetleri başlatır.
- `down`: Çalışan hizmetleri durdurur ve ağları temizler.
- `build`: Hizmetleri yeniden inşa eder.
- `logs`: Hizmetlerin günlüklerini görüntüler.
- `ps`: Çalışan konteynerlerin listesini gösterir.

## Common Examples
Aşağıda `docker-compose` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. **Hizmetleri Başlatma**
   ```bash
   docker-compose up
   ```

2. **Hizmetleri Arka Planda Başlatma**
   ```bash
   docker-compose up -d
   ```

3. **Hizmetleri Durdurma ve Ağları Temizleme**
   ```bash
   docker-compose down
   ```

4. **Hizmetleri Yeniden İnşa Etme**
   ```bash
   docker-compose build
   ```

5. **Hizmet Günlüklerini Görüntüleme**
   ```bash
   docker-compose logs
   ```

## Tips
- `docker-compose.yml` dosyanızı düzenli tutun; bu, yapılandırmanızı daha anlaşılır hale getirir.
- Geliştirme ortamında `-d` seçeneğini kullanarak konteynerleri arka planda çalıştırmak, terminalinizi serbest bırakır.
- Hizmetlerinizi güncellerken `docker-compose up --build` komutunu kullanarak her zaman en son değişiklikleri uyguladığınızdan emin olun.