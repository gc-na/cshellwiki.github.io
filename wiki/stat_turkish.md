# [Linux] Bash stat Kullanımı: Dosya ve dizin bilgilerini görüntüleme

## Overview
`stat` komutu, dosya ve dizinlerin ayrıntılı bilgilerini görüntülemek için kullanılır. Bu bilgiler arasında dosyanın boyutu, oluşturulma tarihi, son erişim tarihi ve izinler gibi özellikler yer alır.

## Usage
Temel kullanım şekli aşağıdaki gibidir:

```bash
stat [options] [arguments]
```

## Common Options
- `-c` veya `--format`: Çıktının formatını belirler.
- `-f` veya `--file-system`: Dosya sistemine ilişkin bilgileri gösterir.
- `--help`: Komutun kullanımına dair yardım bilgilerini görüntüler.
- `--version`: `stat` komutunun sürümünü gösterir.

## Common Examples
Aşağıda `stat` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

### 1. Basit kullanım
Bir dosyanın bilgilerini görüntülemek için:
```bash
stat dosya.txt
```

### 2. Özel format ile görüntüleme
Dosyanın boyutunu ve izinlerini özel bir format ile görüntülemek için:
```bash
stat -c "Boyut: %s, İzinler: %A" dosya.txt
```

### 3. Dizin bilgilerini görüntüleme
Bir dizinin bilgilerini görmek için:
```bash
stat /home/kullanici/
```

### 4. Dosya sistemine dair bilgiler
Dosya sistemine ait bilgileri görüntülemek için:
```bash
stat -f /home/kullanici/
```

## Tips
- `stat` komutunu sık kullanılan dosyalar için bir alias ile kısaltabilirsiniz.
- Çıktıyı daha okunabilir hale getirmek için `-c` seçeneği ile özel formatlar kullanmayı deneyin.
- Dosya izinlerini kontrol etmek için `stat` komutunu kullanmak, güvenlik açısından önemlidir.