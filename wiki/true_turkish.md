# [Linux] Bash true Kullanımı: Her zaman doğru döndürme

## Overview
`true` komutu, her zaman başarıyla (0) dönen bir komuttur. Genellikle bir komutun başarılı bir şekilde tamamlandığını belirtmek veya bir koşulun her zaman doğru olduğu durumlarda kullanılır.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```bash
true [options] [arguments]
```

## Common Options
`true` komutunun herhangi bir seçenek veya argüman almadığını belirtmek önemlidir. Bu komut, sadece çağrıldığında 0 döner.

## Common Examples

### Basit Kullanım
`true` komutunu basit bir şekilde çağırmak:

```bash
true
```

### Koşullu İfadelerde Kullanım
Bir koşulun her zaman doğru olduğunu belirtmek için kullanılabilir:

```bash
if true; then
    echo "Bu her zaman doğru."
fi
```

### Döngülerde Kullanım
Sonsuz bir döngü oluşturmak için `true` kullanılabilir:

```bash
while true; do
    echo "Bu mesaj sürekli basılacak."
    sleep 1
done
```

## Tips
- `true` komutunu, bir betikte belirli bir koşulun her zaman doğru olduğunu belirtmek için kullanabilirsiniz.
- Sonsuz döngülerde dikkatli olun; programın durdurulması gerektiğinde `Ctrl + C` kullanarak döngüyü sonlandırabilirsiniz.
- `true` komutu, test komutları veya koşullu ifadelerde yer tutucu olarak kullanılabilir.