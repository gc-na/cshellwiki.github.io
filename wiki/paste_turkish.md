# [Linux] Bash paste Kullanımı: Dosyaları yan yana birleştirir

## Genel Bakış
`paste` komutu, bir veya daha fazla dosyadaki satırları yan yana birleştirerek yeni bir çıktı oluşturur. Bu, özellikle verileri birleştirmek ve düzenlemek için kullanışlıdır.

## Kullanım
Temel sözdizimi şu şekildedir:

```bash
paste [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-d`: Ayrıştırıcı karakterini belirtir. Varsayılan olarak, satırları tab ile ayırır.
- `-s`: Her dosyanın içeriğini tek bir satırda birleştirir.
- `-z`: Null karakterini ayırıcı olarak kullanır.

## Yaygın Örnekler
1. İki dosyayı tab ile ayırarak birleştirme:
   ```bash
   paste dosya1.txt dosya2.txt
   ```

2. Ayrıştırıcı olarak virgül kullanma:
   ```bash
   paste -d ',' dosya1.txt dosya2.txt
   ```

3. Her dosyanın içeriğini tek bir satırda birleştirme:
   ```bash
   paste -s dosya1.txt dosya2.txt
   ```

4. Birden fazla dosyayı birleştirip çıktı dosyasına yazma:
   ```bash
   paste dosya1.txt dosya2.txt > birlesik_dosya.txt
   ```

## İpuçları
- `paste` komutunu kullanmadan önce dosyaların satır sayılarının eşit olup olmadığını kontrol edin; aksi takdirde, eksik satırlar boş bırakılabilir.
- Ayrıştırıcı karakterini değiştirerek çıktıyı daha okunabilir hale getirebilirsiniz.
- `paste` komutunu, verileri hızlıca birleştirmek için bir boru hattı (`|`) içinde diğer komutlarla birlikte kullanabilirsiniz.