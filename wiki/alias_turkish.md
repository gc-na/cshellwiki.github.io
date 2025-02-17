# [Linux] Bash alias Kullanımı: Komut kısayolları oluşturma

## Genel Bakış
`alias` komutu, Bash kabuğunda sık kullanılan komutlar için kısayollar oluşturmanıza olanak tanır. Bu sayede uzun ve karmaşık komutları daha kısa ve kolay hatırlanabilir hale getirebilirsiniz.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
alias [seçenekler] [kısayol]='[komut]'
```

## Yaygın Seçenekler
- `-p`: Mevcut tüm alias'ları listelemek için kullanılır.

## Yaygın Örnekler
Aşağıda `alias` komutunun bazı pratik örnekleri verilmiştir:

### 1. Basit bir alias oluşturma
```bash
alias ll='ls -la'
```
Bu komut, `ll` yazarak `ls -la` komutunu çalıştırmanızı sağlar.

### 2. Birden fazla alias oluşturma
```bash
alias gs='git status'
alias gc='git commit'
```
Bu komutlar, `gs` yazarak `git status` ve `gc` yazarak `git commit` komutlarını çalıştırmanıza olanak tanır.

### 3. Alias'ları listeleme
```bash
alias -p
```
Bu komut, mevcut tüm alias'ları listelemenizi sağlar.

## İpuçları
- Alias'larınızı `~/.bashrc` veya `~/.bash_aliases` dosyasına ekleyerek, terminalinizi her açtığınızda otomatik olarak yüklenmelerini sağlayabilirsiniz.
- Kısa ve anlamlı isimler kullanarak alias'larınızı daha kolay hatırlayabilirsiniz.
- Alias'larınızı düzenli olarak gözden geçirerek, gereksiz olanları kaldırmayı unutmayın.