# [Linux] Bash renice Kullanımı: Süreç önceliğini değiştirme

## Overview
`renice` komutu, çalışan bir sürecin önceliğini değiştirmek için kullanılır. Bu komut, sistem kaynaklarının daha verimli bir şekilde yönetilmesine yardımcı olur ve belirli süreçlerin diğerlerine göre daha fazla veya daha az kaynak kullanmasını sağlar.

## Usage
Temel sözdizimi şu şekildedir:
```bash
renice [options] [arguments]
```

## Common Options
- `-n`, `--priority`: Yeni öncelik seviyesini belirtir. Bu değer -20 (en yüksek öncelik) ile 19 (en düşük öncelik) arasında olmalıdır.
- `-p`, `--pid`: Önceliği değiştirilecek sürecin PID'sini belirtir.
- `-g`, `--pgroup`: Bir süreç grubunun önceliğini değiştirmek için kullanılır.
- `-u`, `--user`: Belirli bir kullanıcıya ait süreçlerin önceliğini değiştirmek için kullanılır.

## Common Examples
Aşağıda `renice` komutunun bazı pratik örnekleri bulunmaktadır:

1. Belirli bir sürecin önceliğini artırmak:
   ```bash
   renice -n -5 -p 1234
   ```
   Bu komut, PID'si 1234 olan sürecin önceliğini -5 olarak ayarlar.

2. Bir süreç grubunun önceliğini değiştirmek:
   ```bash
   renice -n 10 -g 5678
   ```
   Bu komut, PID'si 5678 olan süreç grubunun önceliğini 10 olarak ayarlar.

3. Belirli bir kullanıcıya ait tüm süreçlerin önceliğini değiştirmek:
   ```bash
   renice -n 15 -u kullanici_adi
   ```
   Bu komut, "kullanici_adi" kullanıcısına ait tüm süreçlerin önceliğini 15 olarak ayarlar.

## Tips
- Öncelik değerlerini dikkatli bir şekilde ayarlayın; yüksek öncelik, sistem kaynaklarının diğer süreçler tarafından kullanılmasını kısıtlayabilir.
- `renice` komutunu kullanmadan önce, sürecin PID'sini öğrenmek için `ps` veya `top` komutlarını kullanabilirsiniz.
- Süreçlerin önceliklerini değiştirmek için genellikle yönetici (root) yetkilerine ihtiyaç duyulur. Bu nedenle, `sudo` ile komutu çalıştırmayı unutmayın.