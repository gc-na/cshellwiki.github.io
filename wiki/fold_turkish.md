# [Linux] Bash fold Kullanımı: Metinleri belirli bir genişlikte katlama

## Overview
`fold` komutu, metin dosyalarındaki satırları belirli bir genişlikte katlayarak daha okunabilir hale getirir. Bu, özellikle uzun satırların daha kısa satırlara bölünmesi gerektiğinde faydalıdır.

## Usage
Temel sözdizimi şu şekildedir:

```bash
fold [options] [arguments]
```

## Common Options
- `-w, --width=N`: Satırların maksimum genişliğini N karakter olarak ayarlar.
- `-s, --spaces`: Katlama işlemini, kelimeleri kesmeden boşluklardan yapar.
- `-b, --bytes`: Genişliği bayt cinsinden ayarlar (varsayılan olarak karakter cinsindendir).

## Common Examples

1. **Temel kullanım**: Bir dosyayı varsayılan genişlikte katlamak.
   ```bash
   fold dosya.txt
   ```

2. **Genişliği ayarlamak**: Satırların genişliğini 50 karakter olarak ayarlamak.
   ```bash
   fold -w 50 dosya.txt
   ```

3. **Boşluklardan katlama**: Kelimeleri kesmeden boşluklardan katlamak.
   ```bash
   fold -s -w 30 dosya.txt
   ```

4. **Çıktıyı bir dosyaya yönlendirmek**: Katlanmış metni yeni bir dosyaya yazmak.
   ```bash
   fold -w 60 dosya.txt > katlanmis_dosya.txt
   ```

## Tips
- Uzun metin dosyalarını okurken `fold` komutunu kullanarak daha iyi bir görünüm elde edebilirsiniz.
- `-s` seçeneği, metinlerin daha anlamlı bir şekilde bölünmesini sağlar; bu nedenle, kelime kesimlerinden kaçınmak için bu seçeneği kullanmayı düşünün.
- `fold` komutunu, diğer komutlarla birleştirerek (örneğin, `cat` ile) daha karmaşık işlemler gerçekleştirebilirsiniz.