# [Linux] Bash getopts Kullanımı: Komut satırı seçeneklerini işlemek için

## Overview
`getopts`, Bash betiklerinde komut satırı argümanlarını işlemek için kullanılan bir yerleşik komuttur. Kullanıcıdan gelen seçenekleri ve argümanları düzenli bir şekilde almak için idealdir. Bu sayede, betiklerinizin daha esnek ve kullanıcı dostu olmasını sağlar.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```bash
getopts [seçenekler] [argümanlar]
```

## Common Options
- `-a`: Seçenekleri bir dizi olarak almak için kullanılır.
- `-b`: Seçeneklerin belirli bir biçimde işlenmesini sağlar.
- `-c`: Komutun nasıl çalışacağını belirlemek için kullanılır.

## Common Examples

### Örnek 1: Basit Seçenek İşleme
Aşağıdaki örnekte, `-f` ve `-v` seçenekleri ile bir dosya adı alınıyor.

```bash
#!/bin/bash

while getopts "fv:" opt; do
  case $opt in
    f)
      echo "Dosya modu seçildi."
      ;;
    v)
      echo "Versiyon: $OPTARG"
      ;;
    \?)
      echo "Geçersiz seçenek: -$OPTARG" >&2
      ;;
  esac
done
```

### Örnek 2: Birden Fazla Seçenek
Bu örnekte, birden fazla seçenek işleniyor.

```bash
#!/bin/bash

while getopts "abc:" opt; do
  case $opt in
    a)
      echo "A seçeneği aktif."
      ;;
    b)
      echo "B seçeneği aktif."
      ;;
    c)
      echo "C seçeneği ile argüman: $OPTARG"
      ;;
    \?)
      echo "Geçersiz seçenek: -$OPTARG" >&2
      ;;
  esac
done
```

### Örnek 3: Varsayılan Değerler
Varsayılan değerler ile seçeneklerin nasıl işleneceğine dair bir örnek.

```bash
#!/bin/bash

verbose=0

while getopts "v" opt; do
  case $opt in
    v)
      verbose=1
      ;;
    \?)
      echo "Geçersiz seçenek: -$OPTARG" >&2
      ;;
  esac
done

if [ $verbose -eq 1 ]; then
  echo "Ayrıntılı mod aktif."
fi
```

## Tips
- Seçeneklerinizi ve argümanlarınızı açık bir şekilde tanımlayın; bu, kullanıcıların betiği daha iyi anlamasına yardımcı olur.
- `getopts` kullanırken, her seçeneğin ne işe yaradığını açıklayan bir yardım mesajı eklemeyi unutmayın.
- Seçeneklerinizi işlemek için `case` yapısını kullanmak, kodunuzu daha düzenli hale getirir ve okunabilirliği artırır.