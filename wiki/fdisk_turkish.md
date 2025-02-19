# [Linux] C Shell (csh) fdisk Kullanımı: Disk bölümlerini yönetme aracı

## Genel Bakış
`fdisk`, disk bölümlerini yönetmek için kullanılan bir komuttur. Bu komut, disk üzerinde yeni bölümler oluşturma, mevcut bölümleri silme veya düzenleme gibi işlemleri gerçekleştirmeye olanak tanır. Genellikle disk yapılandırmalarını değiştirmek veya yeni bir işletim sistemi yüklemek için kullanılır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```
fdisk [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-l`: Tüm diskleri ve bölümleri listele.
- `-u`: Bölüm boyutlarını sektör cinsinden göster.
- `-n`: Yeni bir bölüm oluştur.
- `-d`: Mevcut bir bölümü sil.
- `-p`: Mevcut bölümleri görüntüle.

## Yaygın Örnekler
Aşağıda `fdisk` komutunun bazı pratik örnekleri bulunmaktadır:

### Tüm Diskleri Listeleme
```
fdisk -l
```

### Yeni Bir Bölüm Oluşturma
```
fdisk /dev/sda
```
Bu komut, `/dev/sda` diskinde yeni bir bölüm oluşturmak için `fdisk` aracını başlatır. Ardından, komut isteminde gerekli adımları takip edebilirsiniz.

### Mevcut Bölümleri Görüntüleme
```
fdisk -p /dev/sda
```
Bu komut, `/dev/sda` diskindeki mevcut bölümleri gösterir.

### Bir Bölümü Silme
```
fdisk /dev/sda
```
Yine, bu komut ile `fdisk` aracını başlatıp silmek istediğiniz bölümü seçebilirsiniz.

## İpuçları
- `fdisk` kullanmadan önce önemli verilerinizi yedeklemeyi unutmayın; yanlış işlemler veri kaybına neden olabilir.
- Disk bölümlerini düzenlerken dikkatli olun; yanlış bir işlem sistemin çalışmamasına yol açabilir.
- `fdisk` komutunu kullanmadan önce, hangi disk üzerinde işlem yapacağınızı kesin olarak belirleyin.