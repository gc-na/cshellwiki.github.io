# [Linux] Bash udevadm Kullanımı: Donanım olaylarını yönetme aracı

## Genel Bakış
`udevadm`, Linux sistemlerinde donanım olaylarını yönetmek için kullanılan bir komuttur. Bu komut, udev hizmetiyle etkileşimde bulunarak cihazların tanınması, yönetilmesi ve yapılandırılması süreçlerini kolaylaştırır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
udevadm [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `info`: Belirtilen bir cihaz hakkında bilgi gösterir.
- `trigger`: Udev kurallarını tetikler ve cihazları yeniden tarar.
- `settle`: Cihazların tamamının kurulumunun tamamlanmasını bekler.
- `control`: Udev hizmetinin durumunu kontrol eder.
- `monitor`: Donanım olaylarını gerçek zamanlı olarak izler.

## Yaygın Örnekler
Aşağıda `udevadm` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

### Cihaz Bilgisi Alma
Belirli bir cihaz hakkında bilgi almak için:

```bash
udevadm info --query=all --name=/dev/sda
```

### Cihaz Olaylarını İzleme
Donanım olaylarını gerçek zamanlı olarak izlemek için:

```bash
udevadm monitor
```

### Udev Kurallarını Tetikleme
Tüm cihazların kurallarını yeniden tetiklemek için:

```bash
udevadm trigger
```

### Cihazların Kurulumunu Bekleme
Cihazların kurulumunun tamamlanmasını beklemek için:

```bash
udevadm settle
```

## İpuçları
- `udevadm monitor` komutunu kullanarak, sistemdeki donanım değişikliklerini anlık olarak izleyebilirsiniz.
- Cihaz bilgilerini alırken, `--query=all` seçeneği ile daha fazla detay elde edebilirsiniz.
- Udev kurallarınızı test ederken `trigger` seçeneğini kullanarak, değişikliklerin hemen etkili olup olmadığını kontrol edebilirsiniz.