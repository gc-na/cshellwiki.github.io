# [Linux] C Shell (csh) parted Kullanımı: Disk bölümlerini yönetme aracı

## Genel Bakış
`parted` komutu, disk bölümlerini yönetmek için kullanılan bir araçtır. Bu komut, disk alanını düzenlemek, bölümleri oluşturmak, silmek veya değiştirmek için kullanılır. Kullanıcıların disk yapılandırmalarını kolayca yönetmelerine olanak tanır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```csh
parted [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-l` veya `--list`: Tüm diskleri ve bölümleri listele.
- `mkpart`: Yeni bir bölüm oluştur.
- `rm`: Belirtilen bölümü sil.
- `resizepart`: Bir bölümün boyutunu değiştir.
- `print`: Mevcut bölümleri ve bilgilerini göster.

## Yaygın Örnekler
Aşağıda `parted` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

### Tüm Diskleri Listeleme
```csh
parted -l
```

### Yeni Bir Bölüm Oluşturma
```csh
parted /dev/sda mkpart primary ext4 1MiB 100MiB
```

### Bölüm Silme
```csh
parted /dev/sda rm 1
```

### Bölüm Boyutunu Değiştirme
```csh
parted /dev/sda resizepart 1 200MiB
```

### Mevcut Bölümleri Görüntüleme
```csh
parted /dev/sda print
```

## İpuçları
- `parted` komutunu kullanmadan önce, disk ve bölüm bilgilerinizi yedeklemeyi unutmayın.
- Komutları çalıştırmadan önce, hangi disk üzerinde işlem yapacağınızı dikkatlice kontrol edin.
- `parted` komutunu kullanırken, root yetkilerine sahip olmanız gerektiğini unutmayın.