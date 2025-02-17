# [Linux] Bash update-rc.d Kullanımı: Servislerin başlangıçta yönetimi

## Genel Bakış
`update-rc.d` komutu, Debian tabanlı sistemlerde servislerin başlangıçta otomatik olarak başlatılmasını veya durdurulmasını yönetmek için kullanılır. Bu komut, belirli bir servisin sistem başlangıcında hangi seviyelerde çalışacağını belirlemeye yardımcı olur.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
update-rc.d [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `defaults`: Varsayılan başlangıç seviyelerini kullanarak servisi ekler.
- `remove`: Belirtilen servisi başlangıç listelerinden kaldırır.
- `enable`: Servisi belirtilen seviyelerde etkinleştirir.
- `disable`: Servisi belirtilen seviyelerde devre dışı bırakır.

## Yaygın Örnekler
Aşağıda `update-rc.d` komutunun bazı pratik kullanımları verilmiştir:

### Servis Ekleme
Bir servisi varsayılan başlangıç seviyeleri ile eklemek için:
```bash
sudo update-rc.d myservice defaults
```

### Servis Kaldırma
Bir servisi başlangıç listelerinden kaldırmak için:
```bash
sudo update-rc.d myservice remove
```

### Servisi Etkinleştirme
Bir servisi belirli seviyelerde etkinleştirmek için:
```bash
sudo update-rc.d myservice enable
```

### Servisi Devre Dışı Bırakma
Bir servisi belirli seviyelerde devre dışı bırakmak için:
```bash
sudo update-rc.d myservice disable
```

## İpuçları
- Servislerin doğru bir şekilde yönetilmesi için `update-rc.d` komutunu kullanmadan önce sisteminizdeki mevcut servislerin durumunu kontrol edin.
- Servislerin başlangıç seviyelerini belirlerken dikkatli olun; yanlış bir ayar, sisteminizin başlatılmasında sorunlara yol açabilir.
- `update-rc.d` komutunu kullanmadan önce, ilgili servisin yapılandırma dosyalarını kontrol etmek her zaman iyi bir uygulamadır.