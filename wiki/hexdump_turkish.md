# [Linux] Bash hexdump Kullanımı: Dosyaların ikili gösterimini görüntüleme

## Overview
`hexdump` komutu, dosyaların ikili (binary) verilerini onaltılık (hexadecimal) formatta görüntülemek için kullanılır. Bu, dosyaların içeriğini analiz etmek veya hata ayıklamak için faydalı olabilir.

## Usage
Temel sözdizimi aşağıdaki gibidir:
```bash
hexdump [options] [arguments]
```

## Common Options
- `-C`: Onaltılık ve ASCII gösterimini birlikte görüntüler.
- `-n N`: Sadece ilk N baytı görüntüler.
- `-v`: Tüm veriyi görüntüler, tekrar eden baytları da dahil eder.
- `-e FORMAT`: Özel bir format belirleyerek çıktıyı özelleştirir.

## Common Examples
Aşağıda `hexdump` komutunun bazı yaygın kullanımları verilmiştir:

### 1. Basit Hexdump
Bir dosyanın içeriğini onaltılık formatta görüntülemek için:
```bash
hexdump dosya.txt
```

### 2. Onaltılık ve ASCII Gösterimi
Onaltılık ve ASCII gösterimini birlikte görüntülemek için:
```bash
hexdump -C dosya.txt
```

### 3. İlk N Baytı Görüntüleme
Sadece ilk 16 baytı görüntülemek için:
```bash
hexdump -n 16 dosya.txt
```

### 4. Özel Format ile Çıktı
Özel bir format belirleyerek çıktıyı özelleştirmek için:
```bash
hexdump -e '16/1 "%02x " "\n"' dosya.txt
```

## Tips
- `hexdump` çıktısını daha iyi anlamak için `-C` seçeneğini kullanarak hem onaltılık hem de ASCII çıktısını görüntüleyin.
- Büyük dosyalarla çalışıyorsanız, `-n` seçeneği ile sadece belirli bir bayt aralığını görüntülemek, analiz sürecini hızlandırabilir.
- Çıktıyı bir dosyaya yönlendirmek için `>` operatörünü kullanarak sonuçları kaydedebilirsiniz:
```bash
hexdump dosya.txt > cikti.txt
```