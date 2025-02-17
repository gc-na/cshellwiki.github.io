# [Linux] Bash fdisk Kullanımı: Disk bölümlerini yönetme aracı

## Genel Bakış
`fdisk`, Linux sistemlerinde disk bölümlerini yönetmek için kullanılan bir komut satırı aracıdır. Bu komut, disklerin bölümlendirilmesi, mevcut bölümlerin görüntülenmesi ve yeni bölümlerin oluşturulması gibi işlemleri gerçekleştirmek için kullanılır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
fdisk [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-l`: Tüm diskleri ve bölümlerini listelemek için kullanılır.
- `-u`: Bölüm boyutlarını sektör cinsinden görüntülemek için kullanılır.
- `-n`: Yeni bir bölüm oluşturmak için kullanılır.
- `-d`: Mevcut bir bölümü silmek için kullanılır.
- `-p`: Mevcut bölümlerin bilgilerini görüntülemek için kullanılır.

## Yaygın Örnekler
Aşağıda `fdisk` komutunun bazı pratik örnekleri bulunmaktadır:

### Tüm Diskleri Listeleme
Tüm diskleri ve bölümlerini listelemek için:

```bash
fdisk -l
```

### Yeni Bölüm Oluşturma
Belirli bir diskte yeni bir bölüm oluşturmak için `fdisk` komutunu çalıştırın:

```bash
fdisk /dev/sda
```
Ardından, `n` tuşuna basarak yeni bir bölüm oluşturma adımlarını takip edin.

### Mevcut Bölümü Silme
Bir bölümü silmek için:

```bash
fdisk /dev/sda
```
Ardından, `d` tuşuna basarak silmek istediğiniz bölümü seçin.

### Bölüm Bilgilerini Görüntüleme
Mevcut bölümlerin bilgilerini görüntülemek için:

```bash
fdisk -p /dev/sda
```

## İpuçları
- `fdisk` kullanmadan önce önemli verilerinizi yedeklemeyi unutmayın; yanlış işlemler veri kaybına neden olabilir.
- `fdisk` ile çalışırken dikkatli olun; yanlış bir bölüm silme veya oluşturma işlemi sisteminizi etkileyebilir.
- Disk bölümleme işlemlerinden sonra, değişikliklerin etkili olabilmesi için sistemi yeniden başlatmanız gerekebilir.