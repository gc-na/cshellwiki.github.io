# [Linux] Bash head Kullanımı: Dosya içeriğinin başlangıcını görüntüleme

## Genel Bakış
`head` komutu, bir dosyanın veya birden fazla dosyanın en üstteki birkaç satırını görüntülemek için kullanılır. Genellikle, dosyanın içeriğini hızlıca incelemek amacıyla tercih edilir.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
head [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-n [sayı]`: Görüntülenecek satır sayısını belirtir. Varsayılan olarak ilk 10 satırı gösterir.
- `-c [bayt]`: Görüntülenecek bayt sayısını belirtir.
- `-q`: Birden fazla dosya verildiğinde, dosya isimlerini göstermeden çıktı verir.
- `-v`: Her dosyanın ismini çıktıdan önce gösterir.

## Yaygın Örnekler
1. **Varsayılan 10 satırı görüntüleme:**
   ```bash
   head dosya.txt
   ```

2. **İlk 5 satırı görüntüleme:**
   ```bash
   head -n 5 dosya.txt
   ```

3. **İlk 20 baytı görüntüleme:**
   ```bash
   head -c 20 dosya.txt
   ```

4. **Birden fazla dosyanın ilk 10 satırını görüntüleme:**
   ```bash
   head dosya1.txt dosya2.txt
   ```

5. **Her dosyanın ismini göstererek ilk 3 satırını görüntüleme:**
   ```bash
   head -v -n 3 dosya1.txt dosya2.txt
   ```

## İpuçları
- `head` komutunu, büyük dosyaların içeriğini hızlıca gözden geçirmek için kullanabilirsiniz.
- Dosya içeriğini daha iyi anlamak için `head` komutunu `less` veya `more` gibi diğer komutlarla birleştirebilirsiniz.
- `head` komutunu, bir dosyanın belirli bir kısmını incelemek için sıkça kullanın; bu, zaman kazandırır ve gereksiz verileri göz ardı etmenize yardımcı olur.