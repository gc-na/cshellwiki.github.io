# [Linux] Bash umask Kullanımı: Dosya izinlerini yönetme

## Overview
`umask` komutu, yeni oluşturulan dosya ve dizinlerin varsayılan izinlerini belirlemek için kullanılır. Bu komut, kullanıcıların dosya ve dizinlerine erişim kontrolü sağlamalarına yardımcı olur.

## Usage
Temel sözdizimi şu şekildedir:
```bash
umask [seçenekler] [argümanlar]
```

## Common Options
- `-S`: İzinleri sembolik biçimde gösterir.
- `-p`: Geçerli umask değerini gösterir.
- `-c`: Umask değerini geçici olarak değiştirir.

## Common Examples
1. **Geçerli umask değerini görüntüleme:**
   ```bash
   umask
   ```

2. **Umask değerini ayarlama (örneğin, 022):**
   ```bash
   umask 022
   ```

3. **Umask değerini sembolik olarak görüntüleme:**
   ```bash
   umask -S
   ```

4. **Umask değerini geçici olarak değiştirme:**
   ```bash
   umask -c 077
   ```

## Tips
- Umask değerini ayarlarken, her zaman izinlerin doğru ayarlandığından emin olun; yanlış ayarlar, dosyalarınıza istenmeyen erişimlere yol açabilir.
- Umask değerini `.bashrc` veya `.profile` dosyanıza ekleyerek her oturumda otomatik olarak ayarlanmasını sağlayabilirsiniz.
- Umask değerini belirlerken, genellikle `022` veya `007` gibi değerler kullanılır; bu değerler, dosya ve dizin izinlerini kontrol etmek için yaygın olarak tercih edilir.