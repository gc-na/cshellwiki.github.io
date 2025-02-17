# [Linux] Bash at Kullanımı: Zamanlanmış komutlar çalıştırma

## Genel Bakış
`at` komutu, belirli bir zamanda bir veya daha fazla komutun çalıştırılmasını sağlamak için kullanılır. Bu, zamanlanmış görevlerin kolayca yönetilmesine olanak tanır.

## Kullanım
Temel sözdizimi şu şekildedir:

```bash
at [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-f`: Belirtilen dosyadan komutları alır.
- `-m`: Komut çalıştırıldığında e-posta bildirimi gönderir.
- `-q`: Kuyruk belirler (örneğin, a, b, c).
- `-l`: Zamanlanmış görevlerin listesini gösterir.
- `-d`: Belirtilen görevleri iptal eder.

## Yaygın Örnekler
Aşağıda `at` komutunun bazı pratik örnekleri verilmiştir:

### Örnek 1: Belirli bir zamanda komut çalıştırma
Aşağıdaki komut, 15 dakika sonra `echo "Merhaba Dünya"` komutunu çalıştırır:

```bash
echo "echo 'Merhaba Dünya'" | at now + 15 minutes
```

### Örnek 2: Belirli bir tarihte komut çalıştırma
Aşağıdaki komut, 1 Ocak 2024'te `backup.sh` dosyasını çalıştırır:

```bash
at 01:00 01/01/2024 -f backup.sh
```

### Örnek 3: Zamanlanmış görevlerin listesini görüntüleme
Zamanlanmış görevlerinizi görmek için:

```bash
at -l
```

### Örnek 4: Zamanlanmış bir görevi iptal etme
Belirli bir görevi iptal etmek için:

```bash
at -d [görev numarası]
```

## İpuçları
- `at` komutunu kullanmadan önce, sisteminizde `atd` hizmetinin çalıştığından emin olun.
- Komutlarınızı yazarken dikkatli olun; yanlış bir komut, beklenmedik sonuçlara yol açabilir.
- Zamanlama yaparken, tarih ve saat formatına dikkat edin; yanlış bir format, komutun çalışmamasına neden olabilir.