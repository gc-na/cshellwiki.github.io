# [Linux] Bash bg Kullanımı: Arka planda çalışan işlemleri devam ettirir

## Overview
`bg` komutu, terminalde duraklatılmış bir işlemi arka planda çalıştırmak için kullanılır. Bu, kullanıcıların terminali kullanmaya devam ederken işlemlerin arka planda çalışmasını sağlar.

## Usage
Temel sözdizimi aşağıdaki gibidir:
```bash
bg [options] [arguments]
```

## Common Options
- `job_id`: Belirli bir iş kimliğini belirtir. İş kimliği, `jobs` komutuyla görüntülenebilir.
- `-n`: İşin arka planda çalışmaya başlamadan önce duraklatılmasını sağlar.

## Common Examples
Aşağıda `bg` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. **Duraklatılmış bir işlemi arka planda çalıştırma:**
   ```bash
   bg %1
   ```
   Bu komut, birinci işin arka planda devam etmesini sağlar.

2. **Son duraklatılan işlemi arka planda çalıştırma:**
   ```bash
   bg
   ```
   Bu komut, en son duraklatılan işlemi arka planda başlatır.

3. **Belirli bir iş kimliği ile arka planda çalıştırma:**
   ```bash
   bg %2
   ```
   Bu komut, ikinci işin arka planda devam etmesini sağlar.

## Tips
- `jobs` komutunu kullanarak mevcut duraklatılmış işlemleri görüntüleyebilirsiniz.
- `fg` komutunu kullanarak arka planda çalışan bir işlemi ön plana alabilirsiniz.
- İşlerinizi yönetirken, arka planda çalıştırdığınız işlemlerin durumunu takip etmek için `jobs` komutunu düzenli olarak kontrol edin.