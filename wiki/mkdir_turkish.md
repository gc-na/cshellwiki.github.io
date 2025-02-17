# [Linux] Bash mkdir Kullanımı: Klasör oluşturma komutu

## Genel Bakış
`mkdir` komutu, Linux ve diğer Unix benzeri işletim sistemlerinde yeni dizinler (klasörler) oluşturmak için kullanılır. Kullanıcıların dosya sisteminde düzenli bir yapı kurmalarına yardımcı olur.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
mkdir [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-p`: Ara dizinleri de oluşturur. Eğer belirtilen dizin yolundaki üst dizinler yoksa, bunları da oluşturur.
- `-v`: Oluşturulan dizinlerin adlarını ekrana yazdırır.
- `-m`: Oluşturulan dizin için belirli bir izin ayarı yapar.

## Yaygın Örnekler
Aşağıda `mkdir` komutunun bazı pratik örnekleri verilmiştir:

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

4. Oluşturulan dizinlerin adlarını görüntüleme:
   ```bash
   mkdir -v yeni_klasor
   ```

5. Belirli izinlerle dizin oluşturma:
   ```bash
   mkdir -m 755 yeni_klasor
   ```

## İpuçları
- Dizin oluştururken `-p` seçeneğini kullanarak, birden fazla katmanlı dizin yapısını tek seferde oluşturabilirsiniz.
- Dizin adlarını verirken boşluk kullanıyorsanız, dizin adını tırnak içine almayı unutmayın.
- Dizin oluşturma işlemi sırasında hata almamak için, önceden var olup olmadığını kontrol etmek iyi bir uygulamadır.