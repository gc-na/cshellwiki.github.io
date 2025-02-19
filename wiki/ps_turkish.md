# [Linux] C Shell (csh) ps Kullanımı: Çalışan süreçleri listeleme

## Genel Bakış
`ps` komutu, sistemde çalışan süreçlerin listesini görüntülemek için kullanılır. Bu komut, kullanıcıya hangi süreçlerin aktif olduğunu, bu süreçlerin kim tarafından çalıştırıldığını ve diğer önemli bilgileri sunar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```
ps [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-e`: Tüm süreçleri gösterir.
- `-f`: Tam formatta süreç bilgilerini görüntüler.
- `-u [kullanıcı]`: Belirtilen kullanıcıya ait süreçleri listeler.
- `-p [pid]`: Belirtilen süreç kimliğine (PID) sahip süreci gösterir.

## Yaygın Örnekler
Aşağıda `ps` komutunun bazı pratik örnekleri bulunmaktadır:

1. Tüm süreçleri listeleme:
   ```bash
   ps -e
   ```

2. Tam formatta süreç bilgilerini görüntüleme:
   ```bash
   ps -ef
   ```

3. Belirli bir kullanıcıya ait süreçleri gösterme:
   ```bash
   ps -u kullanıcı_adı
   ```

4. Belirli bir PID'ye sahip süreci görüntüleme:
   ```bash
   ps -p 1234
   ```

## İpuçları
- `ps` komutunu `grep` ile birleştirerek belirli bir süreci arayabilirsiniz:
  ```bash
  ps -ef | grep süreç_adı
  ```
- `ps` çıktısını daha okunabilir hale getirmek için `less` komutuyla birleştirebilirsiniz:
  ```bash
  ps -ef | less
  ```
- Süreçlerin sürekli güncellenen bir listesini görmek için `top` veya `htop` komutlarını kullanmayı düşünebilirsiniz.