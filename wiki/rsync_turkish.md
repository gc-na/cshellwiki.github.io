# [Linux] Bash rsync Kullanımı: Dosya senkronizasyonu

## Genel Bakış
`rsync`, dosyaları ve dizinleri yerel veya uzak sistemler arasında senkronize etmek için kullanılan güçlü bir komut satırı aracıdır. Özellikle büyük dosyaların veya dizinlerin kopyalanması gerektiğinde, sadece değişen kısımları aktararak zaman ve bant genişliği tasarrufu sağlar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
rsync [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-a`: Arşiv modunu etkinleştirir, dosya izinleri, zaman damgaları ve sembolik bağlantılar gibi bilgileri korur.
- `-v`: Ayrıntılı çıktı sağlar, hangi dosyaların kopyalandığını gösterir.
- `-z`: Aktarım sırasında dosyaları sıkıştırır, bu da bant genişliğinden tasarruf sağlar.
- `-r`: Alt dizinler dahil olmak üzere dizinleri kopyalar.
- `--delete`: Hedef dizinde, kaynakta olmayan dosyaları siler.

## Yaygın Örnekler
1. **Yerel dosyaları kopyalama:**
   ```bash
   rsync -av /kaynak/dizin/ /hedef/dizin/
   ```

2. **Uzak bir sunucuya dosya gönderme:**
   ```bash
   rsync -av /yerel/dosya.txt kullanıcı@sunucu:/uzak/dizin/
   ```

3. **Uzak bir sunucudan dosya alma:**
   ```bash
   rsync -av kullanıcı@sunucu:/uzak/dosya.txt /yerel/dizin/
   ```

4. **Sıkıştırma ile dosya kopyalama:**
   ```bash
   rsync -avz /kaynak/dizin/ /hedef/dizin/
   ```

5. **Hedefteki fazladan dosyaları silme:**
   ```bash
   rsync -av --delete /kaynak/dizin/ /hedef/dizin/
   ```

## İpuçları
- `rsync` kullanırken, hedef dizinin sonuna `/` eklemek, kaynak dizinin içeriğini kopyalamak için önemlidir.
- Büyük dosyalarla çalışıyorsanız, `-z` seçeneğini kullanarak aktarım sırasında sıkıştırma yapmayı düşünebilirsiniz.
- `--dry-run` seçeneği ile işlemi gerçekleştirmeden önce ne olacağını görmek için bir deneme yapabilirsiniz. Bu, yanlışlıkla dosyaları silmekten kaçınmanıza yardımcı olur.