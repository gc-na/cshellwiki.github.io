# [Linux] Bash systemctl Kullanımı: Sistem hizmetlerini yönetme aracı

## Genel Bakış
`systemctl`, Linux sistemlerinde hizmetleri ve sistem durumunu yönetmek için kullanılan bir komuttur. Bu komut, sistemd tabanlı sistemlerde hizmetleri başlatma, durdurma, yeniden başlatma ve durumlarını kontrol etme gibi işlemleri gerçekleştirmeye olanak tanır.

## Kullanım
Temel sözdizimi şu şekildedir:
```bash
systemctl [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `start`: Belirtilen hizmeti başlatır.
- `stop`: Belirtilen hizmeti durdurur.
- `restart`: Belirtilen hizmeti yeniden başlatır.
- `status`: Belirtilen hizmetin durumunu gösterir.
- `enable`: Hizmeti sistem başlangıcında otomatik olarak başlatacak şekilde ayarlar.
- `disable`: Hizmetin otomatik olarak başlatılmasını engeller.

## Yaygın Örnekler
Aşağıda `systemctl` komutunun bazı pratik kullanım örnekleri verilmiştir:

### Hizmeti Başlatma
```bash
sudo systemctl start nginx
```

### Hizmeti Durdurma
```bash
sudo systemctl stop nginx
```

### Hizmeti Yeniden Başlatma
```bash
sudo systemctl restart nginx
```

### Hizmetin Durumunu Kontrol Etme
```bash
sudo systemctl status nginx
```

### Hizmeti Otomatik Başlatma
```bash
sudo systemctl enable nginx
```

### Hizmeti Otomatik Başlatmadan Kaldırma
```bash
sudo systemctl disable nginx
```

## İpuçları
- Hizmetlerin durumunu kontrol etmek için `status` seçeneğini kullanarak sorunları hızlıca tespit edebilirsiniz.
- `systemctl` komutunu kullanırken `sudo` yetkilerine ihtiyaç duyabilirsiniz, bu nedenle komutları yönetici olarak çalıştırmayı unutmayın.
- Hizmetlerin günlüklerini görmek için `journalctl` komutunu kullanarak daha fazla bilgi edinebilirsiniz.