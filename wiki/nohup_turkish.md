# [Linux] Bash nohup Kullanımı: Arka planda süreçleri çalıştırma

## Overview
`nohup` komutu, bir işlemi terminalden bağımsız olarak çalıştırmak için kullanılır. Bu komut, terminal kapatılsa bile işlemin devam etmesini sağlar. Genellikle uzun süren işlemler için tercih edilir.

## Usage
Temel sözdizimi şu şekildedir:

```bash
nohup [options] [arguments]
```

## Common Options
- `&`: İşlemi arka planda çalıştırmak için kullanılır.
- `-h`: Kullanım bilgilerini gösterir.
- `-v`: Detaylı bilgi verir.

## Common Examples
1. Basit bir komut çalıştırma:
   ```bash
   nohup sleep 60 &
   ```
   Bu komut, 60 saniye boyunca uykuya dalan bir işlemi arka planda çalıştırır.

2. Bir Python betiğini çalıştırma:
   ```bash
   nohup python my_script.py &
   ```
   `my_script.py` adlı Python betiği, terminal kapatılsa bile çalışmaya devam eder.

3. Çıktıyı bir dosyaya yönlendirme:
   ```bash
   nohup my_command > output.log &
   ```
   Bu komut, `my_command` işleminin çıktısını `output.log` dosyasına kaydeder.

## Tips
- `nohup` ile çalıştırılan işlemlerin çıktısını takip etmek için yönlendirme kullanmayı unutmayın.
- İşlemi arka planda çalıştırmak için `&` kullanmayı ihmal etmeyin.
- `jobs` komutunu kullanarak arka planda çalışan işlemlerinizi kontrol edebilirsiniz.