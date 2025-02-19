# [Linux] C Shell (csh) nl Kullanımı: Satır numaraları ekleme

## Overview
`nl` komutu, bir dosyanın içeriğine satır numaraları ekleyerek çıktısını oluşturur. Bu, metin dosyalarını daha okunabilir hale getirmek için kullanışlıdır.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```
nl [options] [arguments]
```

## Common Options
- `-b`: Satır numarası ekleme biçimini belirler. Örneğin, `-b a` tüm satırlara numara ekler.
- `-f`: Boş satırların numaralandırılmasını kontrol eder. `-f n` ile boş satırlar numaralandırılmaz.
- `-n`: Satır numaralarının biçimini belirler. `-n ln` ile numaralar sola yaslanır.
- `-w`: Satır numaralarının genişliğini ayarlar. Örneğin, `-w 3` ile numaralar 3 karakter genişliğinde olur.

## Common Examples
Aşağıda `nl` komutunun bazı pratik örnekleri bulunmaktadır:

1. **Temel Kullanım:**
   Bir dosyadaki satırları numaralandırmak için:
   ```bash
   nl dosya.txt
   ```

2. **Boş Satırları Atlamak:**
   Boş satırları numaralandırmadan atlamak için:
   ```bash
   nl -b n dosya.txt
   ```

3. **Satır Numarası Biçimini Belirlemek:**
   Satır numaralarını sağa yaslamak için:
   ```bash
   nl -n rn dosya.txt
   ```

4. **Satır Numarası Genişliğini Ayarlamak:**
   Satır numaralarının genişliğini 4 karakter yapmak için:
   ```bash
   nl -w 4 dosya.txt
   ```

## Tips
- `nl` komutunu kullanırken, dosyanızın içeriğini daha iyi anlamak için farklı seçenekleri deneyin.
- Uzun dosyalar için, çıktıyı bir dosyaya yönlendirmek için `>` operatörünü kullanabilirsiniz:
  ```bash
  nl dosya.txt > numaralandirilmis_dosya.txt
  ```
- `man nl` komutunu kullanarak daha fazla bilgi ve seçeneklere ulaşabilirsiniz.