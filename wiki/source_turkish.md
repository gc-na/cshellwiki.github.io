# [Linux] Bash source Kullanımı: Komut dosyalarını çalıştırma

## Overview
`source` komutu, bir Bash betiğini veya dosyasını mevcut kabuk ortamında çalıştırmak için kullanılır. Bu, betikteki değişkenlerin ve işlevlerin mevcut oturumda tanımlanmasını sağlar, böylece kullanıcı bu değişkenlere ve işlevlere doğrudan erişebilir.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```bash
source [seçenekler] [argümanlar]
```

Alternatif olarak, `.` (nokta) ile de kullanılabilir:

```bash
. [seçenekler] [argümanlar]
```

## Common Options
- `-e`: Hata oluşursa, hata mesajı vermeden devam eder.
- `-u`: Betik dosyasındaki değişkenlerin tanımlı olup olmadığını kontrol eder.

## Common Examples

### 1. Bir betiği çalıştırma
Aşağıdaki komut, `script.sh` adlı bir betiği mevcut kabukta çalıştırır:

```bash
source script.sh
```

### 2. Nokta ile çalıştırma
Aynı işlemi nokta ile de yapabilirsiniz:

```bash
. script.sh
```

### 3. Ortam değişkenlerini ayarlama
Bir betik dosyası içindeki ortam değişkenlerini ayarlamak için `source` kullanabilirsiniz:

```bash
source set_env.sh
```

### 4. Hata kontrolü ile çalıştırma
Hata oluşursa devam etmemek için `-e` seçeneğini kullanabilirsiniz:

```bash
source -e script.sh
```

## Tips
- `source` komutunu, sık kullandığınız ortam değişkenlerini veya işlevleri tanımlayan betikler için kullanmak, her seferinde yeniden tanımlamak zorunda kalmamanız için faydalıdır.
- Betik dosyanızın çalıştığından emin olmak için, dosyanın doğru izinlere sahip olduğundan emin olun.
- `source` komutunu kullanırken, çalıştırdığınız betiğin mevcut kabuk ortamını etkileyebileceğini unutmayın; bu nedenle dikkatli olun.