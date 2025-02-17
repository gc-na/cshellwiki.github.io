# [Linux] Bash awk Kullanımı: Metin işleme aracı

## Genel Bakış
`awk`, metin dosyalarını işlemek ve analiz etmek için kullanılan güçlü bir komut satırı aracıdır. Verileri satır ve sütunlar halinde işleyebilir, belirli kalıplara göre filtreleme yapabilir ve hesaplamalar gerçekleştirebilir.

## Kullanım
Temel sözdizimi şu şekildedir:

```bash
awk [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-F`: Alan ayırıcıyı belirtir. Varsayılan ayırıcı boşluktur.
- `-v`: Değişken tanımlamak için kullanılır.
- `-f`: Bir dosyadan awk komutlarını yüklemek için kullanılır.

## Yaygın Örnekler

### 1. Basit bir metin dosyasını okuma
Aşağıdaki komut, `data.txt` dosyasındaki her satırı ekrana yazdırır.

```bash
awk '{print}' data.txt
```

### 2. Belirli bir alanı yazdırma
Aşağıdaki komut, `data.txt` dosyasının ikinci sütununu yazdırır.

```bash
awk '{print $2}' data.txt
```

### 3. Alan ayırıcı kullanma
Aşağıdaki komut, `;` ile ayrılmış bir dosyadaki üçüncü alanı yazdırır.

```bash
awk -F';' '{print $3}' data.csv
```

### 4. Koşullu filtreleme
Aşağıdaki komut, `data.txt` dosyasındaki yalnızca 50'den büyük olan değerleri yazdırır.

```bash
awk '$1 > 50 {print}' data.txt
```

### 5. Hesaplama yapma
Aşağıdaki komut, `data.txt` dosyasındaki ilk sütundaki sayıların toplamını hesaplar.

```bash
awk '{sum += $1} END {print sum}' data.txt
```

## İpuçları
- `awk` komutlarını daha okunabilir hale getirmek için, karmaşık işlemleri bir dosyaya yazmayı düşünün.
- `awk` ile birlikte `sort` ve `uniq` gibi diğer komutları kullanarak daha karmaşık veri analizleri yapabilirsiniz.
- Alanları ve koşulları dikkatlice tanımlamak, doğru sonuçlar almanızı sağlar.