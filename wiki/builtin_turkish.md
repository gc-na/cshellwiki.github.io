# [Linux] Bash builtin: [gömülü komutları görüntüleme]

## Genel Bakış
`builtin` komutu, Bash kabuğunda yerleşik olarak bulunan komutları görüntülemek için kullanılır. Bu komut, kullanıcıların hangi komutların yerleşik olduğunu ve hangi komutların dışsal olduğunu anlamalarına yardımcı olur.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
builtin [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-p`: Yerleşik komutların tam yolunu gösterir.
- `-f`: Belirtilen bir komutun yerleşik olup olmadığını kontrol eder.

## Yaygın Örnekler
Aşağıda `builtin` komutunun bazı pratik örnekleri bulunmaktadır:

### Örnek 1: Tüm yerleşik komutları listeleme
```bash
compgen -b
```

### Örnek 2: Belirli bir komutun yerleşik olup olmadığını kontrol etme
```bash
builtin -f echo
```

### Örnek 3: Yerleşik komutların tam yolunu görüntüleme
```bash
builtin -p
```

## İpuçları
- `builtin` komutunu kullanarak, hangi komutların yerleşik olduğunu öğrenmek, komutların performansını artırabilir.
- Yerleşik komutları kullanmak, sistem kaynaklarını daha verimli kullanmanıza yardımcı olabilir.
- Eğer bir komutun yerleşik versiyonunu kullanmak istiyorsanız, `builtin` ön ekini eklemeyi unutmayın.