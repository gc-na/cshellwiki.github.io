# [Linux] C Shell (csh) systemctl Kullanımı: Sistem hizmetlerini yönetme

## Genel Bakış
`systemctl`, Linux sistemlerinde hizmetleri ve birim dosyalarını yönetmek için kullanılan bir komuttur. Bu komut, sistemin durumunu kontrol etme, hizmetleri başlatma veya durdurma gibi işlemleri gerçekleştirmeye olanak tanır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
systemctl [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `start`: Belirtilen hizmeti başlatır.
- `stop`: Belirtilen hizmeti durdurur.
- `restart`: Belirtilen hizmeti yeniden başlatır.
- `status`: Belirtilen hizmetin durumunu gösterir.
- `enable`: Hizmeti sistem başlangıcında otomatik olarak başlatılacak şekilde ayarlar.
- `disable`: Hizmeti sistem başlangıcında otomatik olarak başlatılmayacak şekilde ayarlar.

## Yaygın Örnekler
Aşağıda `systemctl` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

- Bir hizmeti başlatmak için:
```bash
systemctl start httpd
```

- Bir hizmeti durdurmak için:
```bash
systemctl stop httpd
```

- Bir hizmetin durumunu kontrol etmek için:
```bash
systemctl status httpd
```

- Bir hizmeti yeniden başlatmak için:
```bash
systemctl restart httpd
```

- Bir hizmeti otomatik olarak başlatmak için:
```bash
systemctl enable httpd
```

- Bir hizmetin otomatik başlatılmasını devre dışı bırakmak için:
```bash
systemctl disable httpd
```

## İpuçları
- Hizmetlerin durumunu kontrol etmek için `status` seçeneğini kullanarak sorunları hızlıca tespit edebilirsiniz.
- Hizmetlerin otomatik başlatılmasını ayarlamak, sisteminizin her açılışında gerekli hizmetlerin çalışmasını sağlar.
- `systemctl` komutunu kullanırken, yönetici (root) yetkilerine sahip olduğunuzdan emin olun; aksi takdirde bazı komutlar çalışmayabilir.