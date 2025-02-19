# [Linux] C Shell (csh) lsof Kullanımı: Açık dosyaları listeleme

## Genel Bakış
`lsof` (List Open Files) komutu, sistemde açık olan dosyaların ve bunları kullanan süreçlerin listesini gösterir. Bu komut, dosya tanımlayıcılarını, süreç kimliklerini ve dosya yollarını görüntülemek için kullanılır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
lsof [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-u [kullanıcı]`: Belirtilen kullanıcıya ait açık dosyaları listeler.
- `-p [PID]`: Belirtilen süreç kimliğine (PID) ait açık dosyaları gösterir.
- `-i`: Ağ bağlantılarını ve açık soketleri listeler.
- `+D [dizin]`: Belirtilen dizin ve alt dizinlerindeki açık dosyaları gösterir.
- `-t`: Sadece süreç kimliklerini (PID) döndürür.

## Yaygın Örnekler
Aşağıda `lsof` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

- Belirli bir kullanıcıya ait açık dosyaları listeleme:
  ```bash
  lsof -u username
  ```

- Belirli bir süreç kimliğine ait açık dosyaları görüntüleme:
  ```bash
  lsof -p 1234
  ```

- Ağ bağlantılarını listeleme:
  ```bash
  lsof -i
  ```

- Belirli bir dizindeki açık dosyaları gösterme:
  ```bash
  lsof +D /path/to/directory
  ```

- Sadece süreç kimliklerini döndürme:
  ```bash
  lsof -t -i
  ```

## İpuçları
- `lsof` komutunu kullanmadan önce, yeterli izinlere sahip olduğunuzdan emin olun; bazı dosyalar yalnızca root kullanıcı tarafından görüntülenebilir.
- Ağ bağlantılarını izlemek için `lsof -i` komutunu kullanarak hangi süreçlerin hangi portları kullandığını kolayca görebilirsiniz.
- `lsof` çıktısını daha okunabilir hale getirmek için `grep` ile filtreleme yapabilirsiniz. Örneğin, belirli bir dosya adını aramak için:
  ```bash
  lsof | grep filename
  ```