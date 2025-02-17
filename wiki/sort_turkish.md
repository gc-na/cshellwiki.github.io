# [Linux] Bash sort Kullanımı: Dosya içeriğini sıralama

## Genel Bakış
`sort` komutu, bir dosyadaki veya standart girdideki metin satırlarını sıralamak için kullanılır. Bu komut, verileri alfabetik veya sayısal olarak düzenleyerek daha okunabilir hale getirir.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
sort [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-r`: Sıralamayı tersine çevirir (azalan sırada).
- `-n`: Sayısal sıralama yapar.
- `-k`: Belirli bir alanı (kolonu) kullanarak sıralama yapar.
- `-u`: Tekrar eden satırları kaldırarak yalnızca benzersiz satırları gösterir.
- `-o`: Sonuçları belirtilen dosyaya kaydeder.

## Yaygın Örnekler
1. **Temel sıralama**:
   Aşağıdaki komut, `dosya.txt` içindeki satırları alfabetik olarak sıralar.
   ```bash
   sort dosya.txt
   ```

2. **Ters sıralama**:
   `-r` seçeneği ile satırları azalan sırada sıralamak için:
   ```bash
   sort -r dosya.txt
   ```

3. **Sayısal sıralama**:
   Sayıları içeren bir dosyayı sayısal olarak sıralamak için:
   ```bash
   sort -n sayilar.txt
   ```

4. **Belirli bir alan ile sıralama**:
   İkinci alanı kullanarak sıralama yapmak için:
   ```bash
   sort -k2 dosya.txt
   ```

5. **Sonucu bir dosyaya kaydetme**:
   Sıralanmış çıktıyı `sirali_dosya.txt` dosyasına kaydetmek için:
   ```bash
   sort dosya.txt -o sirali_dosya.txt
   ```

## İpuçları
- Sıralama işlemi büyük/küçük harf duyarlıdır. Eğer büyük harfleri göz ardı etmek istiyorsanız `-f` seçeneğini kullanabilirsiniz.
- Sıralama işlemi, varsayılan olarak alfabetik sıralama yapar; sayısal sıralama için `-n` seçeneğini kullanmayı unutmayın.
- Birden fazla dosya sıralamak isterseniz, dosya isimlerini boşlukla ayırarak yazabilirsiniz. `sort dosya1.txt dosya2.txt` gibi.

Bu bilgilerle `sort` komutunu etkili bir şekilde kullanabilirsiniz.