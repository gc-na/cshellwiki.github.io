# [Linux] C Shell (csh) rsync Kullanımı: Dosya senkronizasyonu ve aktarımı

## Genel Bakış
`rsync`, dosyaları ve dizinleri yerel veya uzak sistemler arasında senkronize etmek ve aktarmak için kullanılan güçlü bir komuttur. Verimliliği artırmak için yalnızca değişen verileri aktarır, bu da ağ trafiğini azaltır ve aktarım süresini kısaltır.

## Kullanım
Temel sözdizimi şu şekildedir:
```bash
rsync [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-a`: Arşiv modu; dosyaların tüm özelliklerini (izinler, zaman damgaları vb.) korur.
- `-v`: Ayrıntılı çıktı; işlemin ne yaptığını gösterir.
- `-z`: Aktarım sırasında verileri sıkıştırır.
- `-r`: Dizini ve içindeki tüm dosyaları rekürsif olarak kopyalar.
- `--delete`: Hedef dizinde, kaynakta bulunmayan dosyaları siler.

## Yaygın Örnekler
1. Yerel bir dizinden başka bir dizine dosya kopyalamak:
   ```bash
   rsync -av /kaynak/dizin/ /hedef/dizin/
   ```

2. Uzak bir sunucuya dosya göndermek:
   ```bash
   rsync -av /yerel/dosya.txt kullanıcı@sunucu:/uzak/dizin/
   ```

3. Uzak bir sunucudan yerel bir dizine dosya almak:
   ```bash
   rsync -av kullanıcı@sunucu:/uzak/dosya.txt /yerel/dizin/
   ```

4. Sıkıştırma ile dosya aktarımı yapmak:
   ```bash
   rsync -avz /kaynak/dizin/ kullanıcı@sunucu:/hedef/dizin/
   ```

5. Hedef dizinde kaynakta bulunmayan dosyaları silmek:
   ```bash
   rsync -av --delete /kaynak/dizin/ /hedef/dizin/
   ```

## İpuçları
- Büyük dosyalarla çalışırken `-z` seçeneğini kullanarak aktarım süresini kısaltabilirsiniz.
- `--dry-run` seçeneği ile işlemi gerçekleştirmeden önce nelerin yapılacağını görebilirsiniz.
- Aktarım sırasında bağlantı kesilirse, `rsync` kaldığı yerden devam edebilir; bu nedenle büyük dosyalar için idealdir.