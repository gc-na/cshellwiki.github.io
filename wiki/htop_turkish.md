# [Linux] Bash htop Kullanımı: Sistem kaynaklarını izleme aracı

## Genel Bakış
htop, Linux tabanlı sistemlerde çalışan bir etkileşimli süreç izleme aracıdır. Kullanıcıların sistemdeki işlemleri, bellek kullanımı ve CPU yükünü gerçek zamanlı olarak görüntülemelerine olanak tanır. htop, top komutuna göre daha kullanıcı dostu bir arayüze sahiptir ve kullanıcıların süreçleri daha kolay yönetmesine yardımcı olur.

## Kullanım
htop komutunun temel sözdizimi aşağıdaki gibidir:

```bash
htop [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-h`, `--help`: Yardım bilgilerini gösterir.
- `-s`, `--sort`: Belirtilen bir alana göre sıralama yapar.
- `-p`, `--pid`: Belirtilen işlem kimliklerini izler.
- `-u`, `--user`: Belirtilen kullanıcıya ait işlemleri gösterir.

## Yaygın Örnekler
Aşağıda htop komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. **htop'u başlatmak için:**
   ```bash
   htop
   ```

2. **Belirli bir kullanıcıya ait işlemleri görüntülemek için:**
   ```bash
   htop -u kullanıcı_adı
   ```

3. **Belirli bir işlem kimliğini izlemek için:**
   ```bash
   htop -p 1234
   ```

4. **Sıralama yapmak için (örneğin, bellek kullanımına göre):**
   ```bash
   htop -s MEM%
   ```

## İpuçları
- htop arayüzünde, `F1` tuşuna basarak yardım menüsüne erişebilirsiniz.
- Süreçleri sonlandırmak için, bir işlemi seçip `F9` tuşuna basarak "SIGKILL" sinyali gönderebilirsiniz.
- Görünüm ayarlarını değiştirmek için `F2` tuşuna basarak yapılandırma menüsüne gidebilirsiniz.
- Performans izleme için htop'u terminalde çalıştırırken, `-d` seçeneği ile güncelleme hızını ayarlayabilirsiniz. Örneğin, her 2 saniyede bir güncellemek için:
  ```bash
  htop -d 2
  ```