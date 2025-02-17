# [Linux] Bash nice Kullanımı: Süreçlerin önceliğini ayarlama

## Overview
`nice` komutu, Unix benzeri işletim sistemlerinde süreçlerin önceliğini ayarlamak için kullanılır. Bu komut, bir sürecin CPU zamanını ne kadar öncelikli alacağını belirler ve böylece sistem kaynaklarının daha verimli kullanılmasına yardımcı olur.

## Usage
Temel sözdizimi şu şekildedir:
```bash
nice [options] [command]
```

## Common Options
- `-n, --adjustment`: Sürecin öncelik seviyesini ayarlamak için kullanılır. Varsayılan olarak 10'dur. Daha düşük bir değer, daha yüksek öncelik anlamına gelir.
- `-h, --help`: Kullanım bilgilerini gösterir.
- `-v, --version`: `nice` komutunun sürüm bilgilerini gösterir.

## Common Examples
Aşağıda `nice` komutunun bazı pratik örnekleri verilmiştir:

1. Varsayılan öncelikle bir komut çalıştırma:
   ```bash
   nice sleep 10
   ```

2. Önceliği artırarak bir komut çalıştırma (örneğin, önceliği 5 olarak ayarlama):
   ```bash
   nice -n 5 my_script.sh
   ```

3. Önceliği azaltarak bir komut çalıştırma (örneğin, önceliği -5 olarak ayarlama):
   ```bash
   nice -n -5 heavy_process
   ```

4. Bir komutun mevcut önceliğini görüntüleme:
   ```bash
   ps -o pid,nice,cmd
   ```

## Tips
- `nice` komutunu kullanırken, sürecin önceliğini çok fazla artırmaktan kaçının, çünkü bu diğer süreçlerin çalışmasını olumsuz etkileyebilir.
- Arka planda çalışan uzun süreli işlemler için `nice` kullanarak sistemin yanıt verme süresini iyileştirebilirsiniz.
- `renice` komutunu kullanarak, zaten çalışan bir sürecin önceliğini değiştirebilirsiniz.