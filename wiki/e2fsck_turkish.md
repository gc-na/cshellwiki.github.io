# [Linux] C Shell (csh) e2fsck Kullanımı: Dosya sistemini kontrol etme aracı

## Genel Bakış
e2fsck, Linux işletim sistemlerinde kullanılan bir komut olup, dosya sistemlerini kontrol etmek ve onarmak için kullanılır. Özellikle ext2, ext3 ve ext4 dosya sistemleri üzerinde çalışır. Bu komut, dosya sistemindeki hataları tespit eder ve düzeltir.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```
e2fsck [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-p`: Hızlı onarım yapar, kullanıcıdan onay istemez.
- `-f`: Dosya sistemini zorla kontrol eder, hataları tespit eder.
- `-y`: Tüm onarım işlemlerini otomatik olarak onaylar.
- `-c`: Dosya sistemindeki blokların kötü olup olmadığını kontrol eder.

## Yaygın Örnekler
1. Bir dosya sistemini kontrol etmek için:
   ```bash
   e2fsck /dev/sda1
   ```

2. Hataları otomatik olarak onarmak için:
   ```bash
   e2fsck -y /dev/sda1
   ```

3. Dosya sistemini zorla kontrol etmek için:
   ```bash
   e2fsck -f /dev/sda1
   ```

4. Kötü blokları kontrol etmek için:
   ```bash
   e2fsck -c /dev/sda1
   ```

## İpuçları
- e2fsck komutunu çalıştırmadan önce dosya sisteminin montajının kaldırıldığından emin olun.
- Önemli verilerinizi yedeklemeyi unutmayın, çünkü bazı onarım işlemleri veri kaybına yol açabilir.
- Hataları düzeltmek için `-y` seçeneğini kullanırken dikkatli olun; bu seçenek tüm onarımları otomatik olarak onaylar.