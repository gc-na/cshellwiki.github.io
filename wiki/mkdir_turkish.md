# [Linux] C Shell (csh) mkdir Kullanımı: Klasör oluşturma komutu

## Overview
`mkdir` komutu, belirtilen isimle yeni bir dizin (klasör) oluşturmak için kullanılır. Bu komut, dosya sisteminde düzen sağlamak ve dosyaları kategorize etmek için oldukça yararlıdır.

## Usage
Temel sözdizimi şu şekildedir:
```
mkdir [options] [arguments]
```

## Common Options
- `-p`: Ana dizin yoksa, ara dizinleri de oluşturarak yeni dizin oluşturur.
- `-m`: Oluşturulan dizinin izinlerini belirlemek için kullanılır. Örneğin, `-m 755` ile dizin oluşturulabilir.
- `-v`: Oluşturulan dizin hakkında bilgi verir. Her oluşturulan dizin için bir çıktı gösterir.

## Common Examples
Aşağıda `mkdir` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. Basit bir dizin oluşturma:
   ```bash
   mkdir yeni_klasor
   ```

2. Birden fazla dizin oluşturma:
   ```bash
   mkdir klasor1 klasor2 klasor3
   ```

3. Ara dizinlerle birlikte dizin oluşturma:
   ```bash
   mkdir -p ana_klasor/alt_klasor
   ```

4. Belirli izinlerle dizin oluşturma:
   ```bash
   mkdir -m 755 ozel_klasor
   ```

5. Oluşturulan dizinler hakkında bilgi alma:
   ```bash
   mkdir -v yeni_klasor
   ```

## Tips
- Dizin oluştururken, dizin adlarının geçerli karakterler içerdiğinden emin olun.
- `-p` seçeneğini kullanarak, birden fazla katmanlı dizin yapısını kolayca oluşturabilirsiniz.
- Dizin oluşturma işlemlerini otomatikleştirmek için bir betik dosyası yazmayı düşünebilirsiniz.