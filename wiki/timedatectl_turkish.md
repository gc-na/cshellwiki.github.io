# [Linux] C Shell (csh) timedatectl Kullanımı: Zaman ve tarih ayarlarını yönetme

## Genel Bakış
`timedatectl` komutu, sistemin zaman ve tarih ayarlarını yönetmek için kullanılır. Bu komut, sistem saatini ayarlamak, zaman dilimini değiştirmek ve NTP (Ağ Zaman Protokolü) senkronizasyonunu kontrol etmek gibi işlevleri yerine getirir.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```csh
timedatectl [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `set-time`: Sistemin saatini ayarlamak için kullanılır.
- `set-timezone`: Zaman dilimini değiştirmek için kullanılır.
- `status`: Mevcut zaman ve tarih ayarlarını görüntüler.
- `list-timezones`: Tüm zaman dilimlerini listeler.
- `set-ntp`: NTP senkronizasyonunu etkinleştirmek veya devre dışı bırakmak için kullanılır.

## Yaygın Örnekler
Sistem saatini ayarlamak için:
```csh
timedatectl set-time '2023-10-01 12:00:00'
```

Zaman dilimini değiştirmek için:
```csh
timedatectl set-timezone Europe/Istanbul
```

Mevcut zaman ve tarih ayarlarını görüntülemek için:
```csh
timedatectl status
```

Tüm zaman dilimlerini listelemek için:
```csh
timedatectl list-timezones
```

NTP senkronizasyonunu etkinleştirmek için:
```csh
timedatectl set-ntp true
```

## İpuçları
- Zaman dilimini ayarlarken doğru zaman dilimini seçtiğinizden emin olun.
- `timedatectl status` komutunu kullanarak sistem saatinin doğru ayarlandığını kontrol edin.
- NTP senkronizasyonunu etkinleştirmek, sistem saatinin her zaman doğru olmasını sağlar, bu nedenle bu seçeneği kullanmayı unutmayın.