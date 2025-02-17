# [Linux] Bash hash Kullanımı: Komutların konumunu görüntüleme

## Genel Bakış
`hash` komutu, Bash kabuğunda daha önce kullanılan komutların konumlarını saklar ve görüntüler. Bu, komutların daha hızlı çalıştırılmasını sağlar çünkü kabuk, komutun tam yolunu her seferinde aramak zorunda kalmaz.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
hash [options] [arguments]
```

## Yaygın Seçenekler
- `-r`: Tüm hash tablosunu sıfırlar.
- `-p`: Belirtilen bir komutun tam yolunu hash tablosuna ekler.
- `-l`: Hash tablosundaki tüm komutların listesini gösterir.

## Yaygın Örnekler

1. **Hash Tablosunu Görüntüleme**
   ```bash
   hash
   ```

2. **Belirli Bir Komutun Yolunu Görüntüleme**
   ```bash
   hash ls
   ```

3. **Hash Tablosunu Sıfırlama**
   ```bash
   hash -r
   ```

4. **Belirli Bir Komutun Yolunu Ekleme**
   ```bash
   hash -p /usr/local/bin/mycommand mycommand
   ```

5. **Hash Tablosundaki Tüm Komutları Listeleme**
   ```bash
   hash -l
   ```

## İpuçları
- `hash` komutunu kullanarak sık kullandığınız komutların yollarını önceden belirleyebilir ve böylece daha hızlı erişim sağlayabilirsiniz.
- Eğer bir komutun yolunu değiştirdiyseniz, hash tablosunu sıfırlamak için `hash -r` komutunu kullanmayı unutmayın.
- `hash` komutunu kullanarak, hangi komutların hangi yollarla çalıştığını kolayca takip edebilirsiniz.