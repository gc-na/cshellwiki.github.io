# [Linux] C Shell (csh) case Kullanımı: Durum kontrolü için bir komut

## Overview
`case` komutu, bir değişkenin içeriğine göre farklı komutlar çalıştırmak için kullanılan bir kontrol yapısıdır. Bu komut, belirli bir değere göre farklı durumları kontrol ederek, program akışını yönlendirmeye olanak tanır.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```csh
case [değişken] in
    [durum1])
        [komutlar]
        ;;
    [durum2])
        [komutlar]
        ;;
    *)
        [varsayılan komutlar]
        ;;
esac
```

## Common Options
`case` komutunun kendine özgü seçenekleri yoktur, ancak kullanılan durumlar için bazı yaygın desenler şunlardır:
- `*` : Herhangi bir değeri temsil eder.
- `?` : Tek bir karakteri temsil eder.
- `[a-z]` : Belirli bir karakter aralığını temsil eder.

## Common Examples

### Örnek 1: Basit durum kontrolü
Aşağıdaki örnekte, bir değişkenin değerine göre farklı mesajlar yazdırılmaktadır.

```csh
set renk = "kırmızı"
case $renk in
    "kırmızı")
        echo "Seçilen renk kırmızı."
        ;;
    "mavi")
        echo "Seçilen renk mavi."
        ;;
    *)
        echo "Bilinmeyen renk."
        ;;
esac
```

### Örnek 2: Kullanıcı girişi kontrolü
Kullanıcıdan alınan bir girdi ile işlem yapmak için `case` komutu kullanılabilir.

```csh
set girdi = $1
case $girdi in
    "başla")
        echo "Program başlatılıyor..."
        ;;
    "dur")
        echo "Program durduruluyor..."
        ;;
    *)
        echo "Geçersiz komut."
        ;;
esac
```

### Örnek 3: Dosya uzantısına göre işlem
Dosya uzantısına göre farklı işlemler yapmak için `case` komutu kullanılabilir.

```csh
set dosya = "belge.txt"
case $dosya in
    *.txt)
        echo "Bu bir metin dosyası."
        ;;
    *.jpg)
        echo "Bu bir resim dosyası."
        ;;
    *)
        echo "Bilinmeyen dosya türü."
        ;;
esac
```

## Tips
- `case` komutunu kullanırken, her durumdan sonra `;;` eklemeyi unutmayın; bu, durumu kapatır.
- Değişkenlerinizi doğru bir şekilde tanımladığınızdan emin olun; aksi takdirde beklenmeyen sonuçlar alabilirsiniz.
- `case` komutunu karmaşık koşullar için kullanmak yerine basit durumlar için tercih edin; karmaşık mantıklar için `if` yapısını kullanmak daha uygun olabilir.