# [Linux] Bash rpm Kullanımı: Paket yönetimi aracı

## Genel Bakış
`rpm` (Red Hat Package Manager), Red Hat tabanlı Linux dağıtımlarında kullanılan bir paket yönetim aracıdır. Yazılım paketlerini kurmak, güncellemek, kaldırmak ve sorgulamak için kullanılır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
rpm [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-i`: Yeni bir RPM paketi kurar.
- `-e`: Yüklenmiş bir RPM paketini kaldırır.
- `-U`: Yüklenmiş bir RPM paketini günceller.
- `-q`: Yüklenmiş bir RPM paketini sorgular.
- `--help`: Komut hakkında yardım bilgisi gösterir.

## Yaygın Örnekler
Paket kurma:
```bash
rpm -i paket_adı.rpm
```

Paket kaldırma:
```bash
rpm -e paket_adı
```

Paket güncelleme:
```bash
rpm -U paket_adı.rpm
```

Yüklenmiş paketleri sorgulama:
```bash
rpm -q paket_adı
```

Tüm yüklenmiş paketleri listeleme:
```bash
rpm -qa
```

## İpuçları
- `rpm` komutunu kullanmadan önce, paketlerin bağımlılıklarını kontrol etmek için `yum` veya `dnf` gibi araçları kullanmak iyi bir uygulamadır.
- Paketlerin doğruluğunu kontrol etmek için `--checksig` seçeneğini kullanarak imzalarını doğrulayabilirsiniz.
- Hatalarla karşılaşırsanız, `--force` seçeneği ile zorla kurulum yapmayı deneyebilirsiniz, ancak bu dikkatli kullanılmalıdır.