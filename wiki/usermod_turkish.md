# [Linux] Bash usermod Kullanımı: Kullanıcı bilgilerini güncelleme

## Overview
`usermod` komutu, Linux sistemlerinde kullanıcı hesaplarını güncellemek için kullanılır. Bu komut, mevcut bir kullanıcının özelliklerini değiştirmek, grup üyeliklerini güncellemek veya kullanıcı adını değiştirmek gibi işlemleri gerçekleştirmeye olanak tanır.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```bash
usermod [seçenekler] [argümanlar]
```

## Common Options
- `-a`: Kullanıcıyı belirtilen gruba ekler (append).
- `-G`: Kullanıcının ait olduğu grupları belirtir.
- `-l`: Kullanıcı adını değiştirir.
- `-d`: Kullanıcının ana dizinini değiştirir.
- `-s`: Kullanıcının varsayılan kabuk ayarını değiştirir.

## Common Examples
Aşağıda `usermod` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. Kullanıcıyı bir gruba eklemek:
   ```bash
   usermod -a -G sudo kullanıcı_adı
   ```

2. Kullanıcı adını değiştirmek:
   ```bash
   usermod -l yeni_kullanıcı_adı eski_kullanıcı_adı
   ```

3. Kullanıcının ana dizinini değiştirmek:
   ```bash
   usermod -d /yeni/ana/dizin kullanıcı_adı
   ```

4. Kullanıcının varsayılan kabuğunu değiştirmek:
   ```bash
   usermod -s /bin/zsh kullanıcı_adı
   ```

## Tips
- `usermod` komutunu kullanmadan önce, değişiklik yapacağınız kullanıcının oturumunun kapalı olduğundan emin olun.
- Değişikliklerin etkili olabilmesi için sistemdeki oturum açma işlemlerini yeniden başlatmak gerekebilir.
- Kullanıcı bilgilerini güncellerken dikkatli olun; yanlış bir değişiklik, kullanıcının sistemdeki erişimini etkileyebilir.