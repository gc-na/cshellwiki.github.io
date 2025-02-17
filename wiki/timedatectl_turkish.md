# [Linux] Bash timedatectl Kullanımı: Sistem tarih ve saatini yönetme

## Overview
`timedatectl`, sistemin tarih ve saat ayarlarını yönetmek için kullanılan bir komuttur. Bu komut, sistem saatini ayarlamanıza, zaman dilimini değiştirmenize ve NTP (Ağ Zaman Protokolü) senkronizasyonunu kontrol etmenize olanak tanır.

## Usage
Temel sözdizimi şu şekildedir:

```bash
timedatectl [options] [arguments]
```

## Common Options
- `status`: Sistem tarih ve saat bilgilerini gösterir.
- `set-time`: Belirtilen tarihi ve saati ayarlar.
- `set-timezone`: Belirtilen zaman dilimini ayarlar.
- `set-ntp`: NTP senkronizasyonunu etkinleştirir veya devre dışı bırakır.
- `list-timezones`: Mevcut zaman dilimlerini listeler.

## Common Examples
Aşağıda `timedatectl` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

### 1. Sistem tarih ve saat bilgilerini görüntüleme
```bash
timedatectl status
```

### 2. Tarih ve saati ayarlama
```bash
timedatectl set-time '2023-10-01 12:00:00'
```

### 3. Zaman dilimini ayarlama
```bash
timedatectl set-timezone Europe/Istanbul
```

### 4. NTP senkronizasyonunu etkinleştirme
```bash
timedatectl set-ntp true
```

### 5. Mevcut zaman dilimlerini listeleme
```bash
timedatectl list-timezones
```

## Tips
- Tarih ve saat ayarlarını yapmadan önce mevcut ayarları kontrol etmek için `timedatectl status` komutunu kullanın.
- Zaman dilimi ayarlarken, doğru zaman dilimini seçtiğinizden emin olun; aksi takdirde tarih ve saat yanlış olabilir.
- NTP senkronizasyonunu etkinleştirerek sistem saatinin otomatik olarak güncel kalmasını sağlayabilirsiniz.