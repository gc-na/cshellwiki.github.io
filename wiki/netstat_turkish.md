# [Linux] Bash netstat Kullanımı: Ağ bağlantılarını ve istatistiklerini görüntüleme

## Genel Bakış
`netstat` komutu, ağ bağlantılarını, yönlendirme tablolarını ve ağ arayüzü istatistiklerini görüntülemek için kullanılan bir araçtır. Bu komut, sistemdeki aktif bağlantılar hakkında bilgi edinmenizi sağlar ve ağ sorunlarını teşhis etmede yardımcı olur.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
netstat [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-a`: Tüm bağlantıları ve dinleme portlarını gösterir.
- `-t`: TCP bağlantılarını gösterir.
- `-u`: UDP bağlantılarını gösterir.
- `-n`: Adresleri ve port numaralarını sayısal olarak gösterir.
- `-l`: Sadece dinleyen soketleri listeler.
- `-p`: Bağlantıların hangi süreç tarafından kullanıldığını gösterir.

## Yaygın Örnekler
Aşağıda `netstat` komutunun bazı pratik örnekleri bulunmaktadır:

1. **Tüm aktif bağlantıları görüntüleme:**
   ```bash
   netstat -a
   ```

2. **Sadece TCP bağlantılarını listeleme:**
   ```bash
   netstat -t
   ```

3. **UDP bağlantılarını görüntüleme:**
   ```bash
   netstat -u
   ```

4. **Dinleyen portları gösterme:**
   ```bash
   netstat -l
   ```

5. **Bağlantıların süreç bilgileriyle birlikte gösterilmesi:**
   ```bash
   netstat -p
   ```

6. **Sayısal adreslerle bağlantıları görüntüleme:**
   ```bash
   netstat -n
   ```

## İpuçları
- `netstat` komutunu sık sık kullanıyorsanız, belirli seçenekleri birleştirerek daha fazla bilgi elde edebilirsiniz. Örneğin, `netstat -tuln` komutuyla hem TCP hem de UDP dinleyen portları sayısal olarak görebilirsiniz.
- Ağ sorunlarını teşhis ederken, `netstat` çıktısını `grep` ile filtreleyerek belirli bağlantıları aramak faydalı olabilir. Örneğin:
  ```bash
  netstat -tuln | grep 80
  ```
- `netstat` komutunun çıktısını daha okunabilir hale getirmek için `less` gibi bir sayfalayıcı ile kullanabilirsiniz:
  ```bash
  netstat -a | less
  ```