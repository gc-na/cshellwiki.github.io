# [Linux] C Shell (csh) last komutu: Kullanıcı oturumlarını görüntüleme

## Genel Bakış
`last` komutu, sistemdeki kullanıcı oturumlarının geçmişini görüntülemek için kullanılır. Bu komut, kullanıcıların ne zaman giriş yaptığını ve ne zaman çıktığını gösterir, ayrıca sistem yeniden başlatmalarını da listeler.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```csh
last [options] [arguments]
```

## Yaygın Seçenekler
- `-n [number]`: Son [number] oturumu gösterir.
- `-R`: Host adlarını gizler.
- `-x`: Sistem yeniden başlatmalarını ve kapanmalarını gösterir.

## Yaygın Örnekler
Aşağıda `last` komutunun bazı pratik örnekleri bulunmaktadır:

1. Tüm kullanıcı oturumlarını görüntüleme:
   ```csh
   last
   ```

2. Son 5 oturumu görüntüleme:
   ```csh
   last -n 5
   ```

3. Sistem yeniden başlatmalarını ve kapanmalarını gösterme:
   ```csh
   last -x
   ```

4. Belirli bir kullanıcı için oturumları görüntüleme:
   ```csh
   last username
   ```

## İpuçları
- `last` komutunu düzenli olarak kullanarak sistemdeki kullanıcı etkinliklerini takip edebilirsiniz.
- Özellikle çok kullanıcılı sistemlerde, kullanıcıların oturum sürelerini izlemek için faydalıdır.
- Çıktıyı daha okunabilir hale getirmek için `less` komutuyla birleştirebilirsiniz:
  ```csh
  last | less
  ```