# [Linux] C Shell (csh) update-rc.d Kullanımı: Hizmetleri başlatma ve durdurma

## Genel Bakış
`update-rc.d` komutu, Debian tabanlı sistemlerde hizmetlerin başlangıç ve kapanış işlemlerini yönetmek için kullanılır. Bu komut, sistemin başlangıcında ve kapanışında hangi hizmetlerin çalıştırılacağını belirlemeye yardımcı olur.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```csh
update-rc.d [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `defaults`: Varsayılan başlangıç ve kapanış seviyelerini ayarlar.
- `remove`: Belirtilen hizmeti başlangıç listelerinden kaldırır.
- `enable`: Hizmeti başlangıçta etkinleştirir.
- `disable`: Hizmeti başlangıçta devre dışı bırakır.

## Yaygın Örnekler
Aşağıda `update-rc.d` komutunun bazı pratik örnekleri verilmiştir:

1. Varsayılan ayarlarla bir hizmet eklemek:
   ```csh
   update-rc.d myservice defaults
   ```

2. Bir hizmeti başlangıç listelerinden kaldırmak:
   ```csh
   update-rc.d myservice remove
   ```

3. Bir hizmeti başlangıçta etkinleştirmek:
   ```csh
   update-rc.d myservice enable
   ```

4. Bir hizmeti başlangıçta devre dışı bırakmak:
   ```csh
   update-rc.d myservice disable
   ```

## İpuçları
- Hizmetlerinizi yönetirken, her zaman `remove` seçeneğini kullanmadan önce dikkatli olun. Yanlışlıkla önemli bir hizmeti kaldırmak istemezsiniz.
- `update-rc.d` komutunu kullanmadan önce, hizmetinizin doğru bir şekilde yapılandırıldığından emin olun.
- Değişikliklerinizi test etmek için sistemi yeniden başlatmadan önce `service` komutunu kullanarak hizmetlerin durumunu kontrol edin.