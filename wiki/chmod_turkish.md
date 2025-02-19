# [Linux] C Shell (csh) chmod Kullanımı: Dosya izinlerini değiştirme

## Overview
`chmod` komutu, dosya ve dizinlerin erişim izinlerini değiştirmek için kullanılır. Bu komut sayesinde, kullanıcıların dosyalara erişim haklarını belirleyebilir ve yönetebilirsiniz.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```csh
chmod [options] [arguments]
```

## Common Options
- `-R`: Alt dizinler dahil olmak üzere, belirtilen dizindeki tüm dosyalara izinleri uygular.
- `u`: Dosya sahibinin izinlerini belirtir (user).
- `g`: Dosya grubunun izinlerini belirtir (group).
- `o`: Diğer kullanıcıların izinlerini belirtir (others).
- `+`: İzin ekler.
- `-`: İzin kaldırır.
- `=`: İzinleri belirli bir değere ayarlar.

## Common Examples
Aşağıda `chmod` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. **Bir dosyaya tüm kullanıcılar için okuma izni verme:**
   ```csh
   chmod a+r dosya.txt
   ```

2. **Bir dosyadan yazma iznini kaldırma:**
   ```csh
   chmod u-w dosya.txt
   ```

3. **Bir dizindeki tüm dosyalara okuma ve yazma izni verme:**
   ```csh
   chmod -R u+rw dizin/
   ```

4. **Bir dosyayı yalnızca sahibi tarafından okunabilir hale getirme:**
   ```csh
   chmod 400 dosya.txt
   ```

5. **Bir dosyaya çalıştırma izni verme:**
   ```csh
   chmod +x script.sh
   ```

## Tips
- İzinleri ayarlarken dikkatli olun; yanlış izinler dosyalarınıza erişimi kısıtlayabilir veya güvenlik açıklarına neden olabilir.
- `ls -l` komutunu kullanarak dosya izinlerinizi kontrol edin.
- İzinleri ayarlarken, `-R` seçeneğini kullanıyorsanız, alt dizinlerdeki dosyaların da etkileneceğini unutmayın.