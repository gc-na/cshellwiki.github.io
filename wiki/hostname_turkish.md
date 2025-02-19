# [Linux] C Shell (csh) hostname Kullanımı: Sistem adını görüntüleme ve ayarlama

## Overview
`hostname` komutu, sistemin ağ üzerindeki adını görüntülemek veya değiştirmek için kullanılır. Bu komut, özellikle ağ yapılandırmalarında ve sistem yönetiminde önemli bir rol oynar.

## Usage
Temel sözdizimi şu şekildedir:

```csh
hostname [options] [arguments]
```

## Common Options
- `-f`: Tam alan adı (FQDN) ile sistem adını gösterir.
- `-s`: Sadece kısa sistem adını gösterir.
- `-i`: IP adresini gösterir.
- `-V`: Versiyon bilgisini gösterir.

## Common Examples
Aşağıda `hostname` komutunun bazı pratik örnekleri bulunmaktadır:

1. **Sistem adını görüntüleme:**
   ```csh
   hostname
   ```

2. **Kısa sistem adını görüntüleme:**
   ```csh
   hostname -s
   ```

3. **Tam alan adı ile sistem adını görüntüleme:**
   ```csh
   hostname -f
   ```

4. **Sistemin IP adresini görüntüleme:**
   ```csh
   hostname -i
   ```

5. **Sistem adını değiştirme:**
   ```csh
   hostname yeni-sistem-adi
   ```

## Tips
- Sistem adını değiştirdikten sonra, değişikliğin etkili olması için bazı durumlarda sistemi yeniden başlatmanız gerekebilir.
- Ağ ayarlarını güncellerken, `hostname` komutunu kullanarak sistem adının doğru olduğundan emin olun.
- `hostname` komutunu kullanırken, gerekli izinlere sahip olduğunuzdan emin olun; bazı sistemlerde yalnızca yönetici kullanıcılar bu komutu kullanabilir.