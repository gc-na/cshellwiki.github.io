# [Linux] C Shell (csh) df Kullanımı: Disk alanı bilgilerini gösterir

## Overview
`df` komutu, dosya sistemlerinin disk alanı kullanımını gösteren bir komuttur. Kullanıcıların, sistemdeki disk alanının ne kadarının kullanıldığını ve ne kadarının boş olduğunu görmesine olanak tanır.

## Usage
Temel sözdizimi şu şekildedir:
```csh
df [options] [arguments]
```

## Common Options
- `-h`: İnsan tarafından okunabilir formatta çıktı verir (örneğin, KB, MB, GB).
- `-T`: Dosya sisteminin türünü gösterir.
- `-a`: Tüm dosya sistemlerini, boş olanlar dahil, listeler.
- `-i`: Dosya sistemindeki inode kullanımını gösterir.

## Common Examples
Aşağıda `df` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. Temel disk alanı bilgilerini gösterme:
   ```csh
   df
   ```

2. İnsan tarafından okunabilir formatta çıktı alma:
   ```csh
   df -h
   ```

3. Belirli bir dosya sisteminin disk alanı kullanımını gösterme:
   ```csh
   df /dev/sda1
   ```

4. Tüm dosya sistemlerinin türlerini gösterme:
   ```csh
   df -T
   ```

5. Inode kullanımını gösterme:
   ```csh
   df -i
   ```

## Tips
- `df` komutunu sık sık kullanarak disk alanı kullanımını izlemek, sistem yönetimi için önemlidir.
- `-h` seçeneği ile çıktıyı daha anlaşılır hale getirmek, özellikle büyük disk alanları ile çalışırken faydalıdır.
- Disk alanı dolmadan önce düzenli olarak kontrol yapmak, sistemin sağlıklı çalışmasını sağlar.