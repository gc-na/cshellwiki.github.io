# [Linux] C Shell (csh) netstat Kullanımı: Ağ bağlantılarını görüntüleme aracı

## Genel Bakış
`netstat` komutu, ağ bağlantılarını, yönlendirme tablolarını ve ağ arayüzü istatistiklerini görüntülemek için kullanılır. Bu komut, sistemdeki aktif bağlantılar hakkında bilgi sağlar ve ağ sorunlarını teşhis etmek için yararlıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
netstat [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-a`: Tüm bağlantıları ve dinleme portlarını gösterir.
- `-n`: Adresleri ve port numaralarını sayısal olarak gösterir.
- `-t`: TCP bağlantılarını gösterir.
- `-u`: UDP bağlantılarını gösterir.
- `-l`: Sadece dinleme durumundaki bağlantıları gösterir.
- `-p`: Bağlantının hangi süreç tarafından kullanıldığını gösterir.

## Yaygın Örnekler
Aşağıda `netstat` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. Tüm aktif bağlantıları ve dinleme portlarını görüntülemek için:
   ```bash
   netstat -a
   ```

2. Sadece TCP bağlantılarını listelemek için:
   ```bash
   netstat -t
   ```

3. Sayısal adreslerle bağlantıları görüntülemek için:
   ```bash
   netstat -n
   ```

4. Dinleme durumundaki bağlantıları görmek için:
   ```bash
   netstat -l
   ```

5. Hangi süreçlerin hangi bağlantıları kullandığını görmek için:
   ```bash
   netstat -p
   ```

## İpuçları
- `netstat` çıktısını daha iyi analiz etmek için `grep` komutunu kullanarak belirli bağlantıları filtreleyebilirsiniz.
- Ağ sorunlarını teşhis ederken, `-n` seçeneğini kullanmak, DNS sorgularını atlayarak daha hızlı sonuç almanızı sağlar.
- `netstat` komutunu düzenli olarak kullanarak sisteminizdeki ağ durumunu takip edebilirsiniz.