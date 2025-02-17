# [Linux] Bash ps Kullanımı: Çalışan süreçleri görüntüleme

## Genel Bakış
`ps` komutu, Linux ve Unix benzeri işletim sistemlerinde çalışan süreçlerin (programların) durumunu görüntülemek için kullanılır. Bu komut, sistemdeki aktif işlemleri ve bu işlemlerle ilgili bilgileri sağlar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
ps [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-e` veya `-A`: Tüm süreçleri gösterir.
- `-f`: Tam bir formatta süreç bilgilerini gösterir.
- `-u [kullanıcı]`: Belirtilen kullanıcıya ait süreçleri listeler.
- `-aux`: Tüm kullanıcıların süreçlerini detaylı bir şekilde gösterir.
- `--sort`: Süreçleri belirli bir kritere göre sıralar.

## Yaygın Örnekler
Aşağıda `ps` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. Tüm süreçleri listeleme:
   ```bash
   ps -e
   ```

2. Belirli bir kullanıcıya ait süreçleri görüntüleme:
   ```bash
   ps -u username
   ```

3. Tüm süreçleri detaylı bir formatta gösterme:
   ```bash
   ps -ef
   ```

4. Süreçleri bellek kullanımına göre sıralama:
   ```bash
   ps aux --sort=-%mem
   ```

5. Belirli bir süreç ID'sine (PID) sahip süreci görüntüleme:
   ```bash
   ps -p 1234
   ```

## İpuçları
- `ps` komutunu `grep` ile birleştirerek belirli bir süreci kolayca bulabilirsiniz:
  ```bash
  ps aux | grep process_name
  ```
- `top` komutunu kullanarak süreçlerin dinamik bir görünümünü elde edebilirsiniz; bu, sürekli güncellenen bir süreç listesi sağlar.
- `man ps` komutunu kullanarak `ps` komutunun tüm seçenekleri ve kullanımları hakkında daha fazla bilgi alabilirsiniz.