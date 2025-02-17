# [Linux] Bash bindkey Kullanımı: Klavye kısayollarını ayarlama

## Overview
`bindkey` komutu, kullanıcıların terminaldeki klavye kısayollarını yapılandırmalarına olanak tanır. Bu komut, özellikle Zsh kabuğunda yaygın olarak kullanılır ve kullanıcıların belirli tuş kombinasyonlarına özel komutlar atamasını sağlar.

## Usage
Temel sözdizimi şu şekildedir:

```bash
bindkey [options] [arguments]
```

## Common Options
- `-e`: Emacs tarzı kısayolları etkinleştirir.
- `-v`: Vi tarzı kısayolları etkinleştirir.
- `-L`: Mevcut tuş bağlamalarını listeler.
- `-s`: Belirli bir tuş kombinasyonuna bir dizi komut atar.

## Common Examples
Aşağıda `bindkey` komutunun bazı pratik örnekleri verilmiştir:

1. **Emacs tarzı kısayolları etkinleştirme:**
   ```bash
   bindkey -e
   ```

2. **Vi tarzı kısayolları etkinleştirme:**
   ```bash
   bindkey -v
   ```

3. **Mevcut tuş bağlamalarını listeleme:**
   ```bash
   bindkey -L
   ```

4. **Belirli bir tuş kombinasyonuna komut atama:**
   ```bash
   bindkey '^x' 'exit'
   ```

5. **Bir dizi komut atama:**
   ```bash
   bindkey -s '^g' 'git status\n'
   ```

## Tips
- Kısayollarınızı düzenli tutmak için sık kullandığınız komutları belirleyin ve bunlara kısayollar atayın.
- `bindkey -L` komutunu kullanarak mevcut kısayollarınızı gözden geçirin ve gereksiz olanları kaldırın.
- Kısayollarınızı bir dosyada saklayarak, terminal ayarlarınızı her açtığınızda otomatik olarak yükleyebilirsiniz.