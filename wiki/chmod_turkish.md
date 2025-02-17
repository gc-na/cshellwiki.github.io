# [Linux] Bash chmod Kullanımı: Dosya ve dizin izinlerini değiştirme

## Genel Bakış
`chmod` komutu, dosya ve dizinlerin erişim izinlerini değiştirmek için kullanılır. Bu komut sayesinde, kullanıcıların dosyalara erişim haklarını belirleyebilir ve güvenlik ayarlarını yönetebilirsiniz.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
chmod [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `u`: Kullanıcı (dosyanın sahibi)
- `g`: Grup (dosyanın ait olduğu grup)
- `o`: Diğerleri (kullanıcı ve grup dışındaki herkes)
- `a`: Hepsi (kullanıcı, grup ve diğerleri)
- `+`: İzin ekler
- `-`: İzin kaldırır
- `=`: İzinleri belirler

## Yaygın Örnekler
1. Kullanıcıya okuma, yazma ve çalıştırma izni verme:
   ```bash
   chmod u+rwx dosya.txt
   ```

2. Gruba yalnızca okuma izni verme:
   ```bash
   chmod g+r dosya.txt
   ```

3. Diğerlerinden yazma iznini kaldırma:
   ```bash
   chmod o-w dosya.txt
   ```

4. Tüm kullanıcılara okuma izni verme:
   ```bash
   chmod a+r dosya.txt
   ```

5. Bir dizindeki tüm dosyalara yazma izni verme:
   ```bash
   chmod -R u+w dizin/
   ```

## İpuçları
- İzinleri ayarlarken dikkatli olun; yanlış izinler güvenlik açıklarına yol açabilir.
- `chmod` komutunu kullanmadan önce mevcut izinleri kontrol etmek için `ls -l` komutunu kullanabilirsiniz.
- İzinleri sayısal olarak ayarlamak için `chmod 755 dosya.txt` gibi bir format kullanabilirsiniz; burada `7` (okuma, yazma, çalıştırma), `5` (okuma, çalıştırma) ve `5` (okuma, çalıştırma) izinlerini temsil eder.