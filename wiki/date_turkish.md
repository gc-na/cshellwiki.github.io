# [Linux] Bash date Kullanımı: Tarih ve saat bilgisi gösterimi

## Overview
`date` komutu, sistemin tarih ve saat bilgilerini görüntülemek için kullanılır. Bu komut, tarih ve saat formatlarını özelleştirmenize de olanak tanır.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```bash
date [options] [arguments]
```

## Common Options
- `+FORMAT`: Tarih ve saat çıktısını belirli bir formatta gösterir.
- `-u`: UTC (Evrensel Koordinat Zamanı) zaman diliminde tarih ve saat gösterir.
- `-d STRING`: Belirtilen tarih ve saat dizesini kullanarak tarih ve saat hesaplar.

## Common Examples
Aşağıda `date` komutunun bazı yaygın kullanım örnekleri verilmiştir:

### 1. Mevcut tarih ve saati görüntüleme
```bash
date
```

### 2. Tarih ve saati belirli bir formatta gösterme
```bash
date "+%Y-%m-%d %H:%M:%S"
```

### 3. UTC zaman diliminde tarih ve saat gösterme
```bash
date -u
```

### 4. Belirli bir tarih ve saat dizesini kullanarak tarih hesaplama
```bash
date -d "next Friday"
```

### 5. Özel format kullanarak tarih ve saat gösterme
```bash
date "+%A, %d %B %Y"
```

## Tips
- Tarih ve saat formatlarını özelleştirirken, `%` işaretini kullanarak farklı bileşenleri belirtebilirsiniz.
- `date` komutunu bir betik içinde kullanarak otomatik tarih ve saat bilgisi alabilirsiniz.
- Tarih ve saat bilgilerini dosya isimlerinde kullanırken, boşluk ve özel karakterlerden kaçınmak için uygun formatları tercih edin.