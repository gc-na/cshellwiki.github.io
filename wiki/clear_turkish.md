# [Linux] Bash clear Kullanımı: Ekranı temizler

## Overview
`clear` komutu, terminal ekranını temizlemek için kullanılır. Bu komut, kullanıcıların daha düzenli bir çalışma alanına sahip olmalarını sağlar ve önceki komutların çıktılarının görünümünü ortadan kaldırır.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```bash
clear [options] [arguments]
```

## Common Options
- `-x`: Ekranı temizlerken, geçmiş komutların kaydını tutar.
- `-s`: Ekranı temizler, ancak ekranın alt kısmındaki satırları korur.

## Common Examples
Aşağıda `clear` komutunun bazı pratik örnekleri bulunmaktadır:

1. Terminal ekranını temizlemek için:
   ```bash
   clear
   ```

2. Ekranı temizlerken geçmişi tutmak için:
   ```bash
   clear -x
   ```

3. Ekranı temizlerken alt satırları korumak için:
   ```bash
   clear -s
   ```

## Tips
- `clear` komutunu sık sık kullanarak terminalinizin daha düzenli görünmesini sağlayabilirsiniz.
- Ekranı temizlemek için `Ctrl + L` kısayolunu da kullanabilirsiniz; bu, `clear` komutuyla aynı etkiyi yaratır.
- Terminalde uzun bir işlem yaptıktan sonra ekranı temizlemek, daha iyi bir odaklanma sağlar.