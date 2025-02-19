# [Linux] C Shell (csh) udevadm Kullanımı: Aygıt yönetimi ve sorgulama aracı

## Genel Bakış
`udevadm`, Linux sistemlerinde aygıt yönetimi ve sorgulama işlemleri için kullanılan bir komuttur. Bu komut, aygıtların durumunu kontrol etmek, aygıt bilgilerini görüntülemek ve udev kurallarını yönetmek için kullanılır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```
udevadm [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `info`: Belirtilen aygıt hakkında bilgi gösterir.
- `trigger`: Udev olaylarını tetikler.
- `settle`: Tüm udev olaylarının tamamlanmasını bekler.
- `control`: Udev daemon'unu kontrol eder.

## Yaygın Örnekler
Aşağıda `udevadm` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

### Aygıt Bilgisi Alma
Belirli bir aygıtın bilgilerini görüntülemek için:
```bash
udevadm info --query=all --name=/dev/sda
```

### Aygıt Olaylarını Tetikleme
Tüm aygıt olaylarını tetiklemek için:
```bash
udevadm trigger
```

### Udev Olaylarının Tamamlanmasını Bekleme
Tüm udev olaylarının tamamlanmasını beklemek için:
```bash
udevadm settle
```

### Udev Daemon'unu Kontrol Etme
Udev daemon'unun durumunu kontrol etmek için:
```bash
udevadm control --reload-rules
```

## İpuçları
- `udevadm info` komutunu kullanarak aygıtların detaylı bilgilerini alabilir ve sorun giderme işlemlerini kolaylaştırabilirsiniz.
- Udev kurallarını değiştirdikten sonra `udevadm control --reload-rules` komutunu kullanarak değişikliklerin etkili olmasını sağlayın.
- Aygıtların durumunu düzenli olarak kontrol etmek, sistem yönetimi açısından faydalıdır.