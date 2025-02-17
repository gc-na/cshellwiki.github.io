# [Linux] Bash e2fsck Kullanımı: Dosya sistemini kontrol etme ve onarma

## Overview
e2fsck, Linux işletim sistemlerinde kullanılan bir komuttur ve ext2, ext3 ve ext4 dosya sistemlerini kontrol etmek ve onarmak için kullanılır. Bu komut, dosya sistemindeki hataları tespit eder ve düzeltir, böylece veri kaybını önlemeye yardımcı olur.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```bash
e2fsck [options] [arguments]
```

## Common Options
- `-p`: Hızlı kontrol yapar ve hataları otomatik olarak düzeltir.
- `-f`: Dosya sisteminin her zaman kontrol edilmesini sağlar, hata varsa düzeltir.
- `-y`: Tüm sorulara "evet" yanıtı verir, bu da tüm hataların otomatik olarak düzeltilmesini sağlar.
- `-c`: Dosya sistemindeki kötü sektörleri kontrol eder ve raporlar.
- `-n`: Dosya sistemini kontrol eder ancak düzeltme yapmaz.

## Common Examples
Aşağıda e2fsck komutunun bazı pratik örnekleri bulunmaktadır:

### Temel Kontrol
Dosya sistemini kontrol etmek için:

```bash
e2fsck /dev/sda1
```

### Hızlı Kontrol ve Düzeltme
Hataları otomatik olarak düzeltmek için:

```bash
e2fsck -p /dev/sda1
```

### Kötü Sektör Kontrolü
Kötü sektörleri kontrol etmek için:

```bash
e2fsck -c /dev/sda1
```

### Tüm Sorulara Evet
Tüm hataları otomatik olarak düzeltmek için:

```bash
e2fsck -y /dev/sda1
```

## Tips
- e2fsck komutunu çalıştırmadan önce dosya sisteminin montajlı olmadığından emin olun. Aksi takdirde, veri kaybı yaşanabilir.
- Düzenli olarak dosya sisteminizi kontrol etmek, olası hataların önüne geçmek için iyi bir uygulamadır.
- Eğer büyük bir dosya sisteminiz varsa, işlemin uzun sürebileceğini unutmayın; bu nedenle, işlemi mümkünse bakım zamanlarında yapın.