# [Linux] C Shell (csh) at: Zamanlanmış görevler oluşturma

## Overview
`at` komutu, belirli bir zamanda bir komut veya komut dizisini çalıştırmak için kullanılır. Bu, kullanıcıların belirli bir zaman diliminde otomatik olarak görevler planlamasına olanak tanır.

## Usage
Temel sözdizimi aşağıdaki gibidir:
```
at [options] [arguments]
```

## Common Options
- `-f` : Belirtilen dosyadan komutları okur.
- `-l` : Planlanmış görevlerin listesini gösterir.
- `-d` : Belirtilen görevleri iptal eder.
- `-m` : Görev tamamlandığında e-posta bildirimi gönderir.

## Common Examples
Aşağıda `at` komutunun bazı pratik örnekleri bulunmaktadır:

1. **Basit bir komut zamanlama**:
   Belirli bir zamanda `echo` komutunu çalıştırmak için:
   ```bash
   echo "Merhaba, dünya!" | at 14:00
   ```

2. **Bir dosyadan komut okuma**:
   `komutlar.txt` dosyasındaki komutları belirli bir zamanda çalıştırmak için:
   ```bash
   at -f komutlar.txt 15:00
   ```

3. **Planlanmış görevlerin listesini görüntüleme**:
   Daha önce planlanmış görevleri görmek için:
   ```bash
   at -l
   ```

4. **Bir görevi iptal etme**:
   Görev numarası 2 olan bir görevi iptal etmek için:
   ```bash
   atrm 2
   ```

## Tips
- `at` komutunu kullanmadan önce, sisteminizde `atd` hizmetinin çalıştığından emin olun.
- Görevlerinizi zamanlamadan önce, doğru zaman formatını kullandığınızdan emin olun.
- Uzun süreli görevler için, e-posta bildirimini kullanarak görevlerin durumunu takip edebilirsiniz.