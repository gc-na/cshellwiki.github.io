# [Linux] Bash sed Kullanımı: Metin düzenleme aracı

## Genel Bakış
`sed`, akış düzenleyici (stream editor) olarak bilinen bir komuttur. Metin dosyalarını veya standart girdi akışını düzenlemek için kullanılır. `sed`, metin üzerinde arama, değiştirme, silme ve ekleme gibi işlemleri gerçekleştirebilir.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
sed [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-e`: Birden fazla komut belirtmek için kullanılır.
- `-i`: Değişiklikleri doğrudan dosyada yapar (yerinde düzenleme).
- `-n`: Varsayılan olarak çıktı üretmez, yalnızca belirtilen komutlarla çıktı üretir.
- `s/pattern/replacement/`: Belirtilen deseni bulur ve yerine yeni bir metin koyar.

## Yaygın Örnekler
1. **Basit Değiştirme**
   Bir dosyadaki "eski" kelimesini "yeni" ile değiştirmek için:
   ```bash
   sed 's/eski/yeni/' dosya.txt
   ```

2. **Yerinde Değiştirme**
   "eski" kelimesini "yeni" ile değiştirmek ve değişiklikleri dosyada kaydetmek için:
   ```bash
   sed -i 's/eski/yeni/' dosya.txt
   ```

3. **Belirli Satırları Yazdırma**
   Sadece 2. satırı yazdırmak için:
   ```bash
   sed -n '2p' dosya.txt
   ```

4. **Birden Fazla Değişiklik**
   Hem "eski" kelimesini "yeni" ile hem de "başka" kelimesini "farklı" ile değiştirmek için:
   ```bash
   sed -e 's/eski/yeni/' -e 's/başka/farklı/' dosya.txt
   ```

5. **Satır Silme**
   3. satırı silmek için:
   ```bash
   sed '3d' dosya.txt
   ```

## İpuçları
- `-i` seçeneğini kullanırken dikkatli olun; dosyadaki veriler geri alınamaz şekilde değiştirilecektir.
- Değişiklikleri test etmek için önce `-n` seçeneğini kullanarak çıktıyı kontrol edin.
- `sed` komutlarını bir dosyaya kaydetmek için `-f` seçeneğini kullanarak bir komut dosyası oluşturabilirsiniz.