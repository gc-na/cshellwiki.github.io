# [Linux] C Shell (csh) nice Kullanımı: İşlem önceliğini ayarlama

## Overview
`nice` komutu, bir işlemin CPU zamanını nasıl kullanacağını belirlemek için işlem önceliğini ayarlamak amacıyla kullanılır. Bu komut, sistem kaynaklarının daha verimli bir şekilde kullanılmasına yardımcı olur.

## Usage
Temel sözdizimi aşağıdaki gibidir:
```
nice [options] [arguments]
```

## Common Options
- `-n` veya `--adjustment`: İşlem önceliğini ayarlamak için bir değer belirtir. Bu değer -20 ile 19 arasında olabilir. -20 en yüksek önceliği, 19 ise en düşük önceliği temsil eder.
- `-h` veya `--help`: Komut hakkında yardım bilgilerini gösterir.
- `-v` veya `--version`: Komutun sürüm bilgilerini gösterir.

## Common Examples
1. **Varsayılan öncelikle bir komut çalıştırma:**
   ```csh
   nice mycommand
   ```

2. **Önceliği artırarak bir komut çalıştırma:**
   ```csh
   nice -n -5 mycommand
   ```

3. **Önceliği azaltarak bir komut çalıştırma:**
   ```csh
   nice -n 10 mycommand
   ```

4. **Bir komutun önceliğini kontrol etme:**
   ```csh
   ps -o pid,nice,cmd
   ```

## Tips
- `nice` komutunu kullanarak sistem kaynaklarını daha verimli bir şekilde yönetebilirsiniz. Özellikle yoğun işlem yükü altında çalışan sistemlerde, düşük öncelikli işlemler için `nice` kullanmak faydalı olabilir.
- İşlemlerin önceliğini ayarlarken, sistemin genel performansını etkilememek için dikkatli olun.
- `renice` komutunu kullanarak zaten çalışan bir işlemin önceliğini değiştirebilirsiniz.