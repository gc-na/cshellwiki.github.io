# [Linux] Bash vigr Uso: Editar arquivos de configuração de forma segura

## Overview
O comando `vigr` é uma ferramenta utilizada para editar arquivos de configuração do sistema, como o `/etc/passwd` e o `/etc/group`, de maneira segura. Ele garante que o arquivo seja bloqueado durante a edição, evitando que múltiplos usuários o modifiquem ao mesmo tempo, o que poderia causar corrupção de dados.

## Usage
A sintaxe básica do comando `vigr` é a seguinte:

```bash
vigr [opções] [arquivo]
```

## Common Options
- `-h`, `--help`: Exibe a ajuda do comando.
- `-o`, `--editor`: Especifica um editor alternativo para usar em vez do editor padrão.
- `-s`, `--safe`: Ativa o modo seguro, que impede a edição de arquivos que não são de configuração.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `vigr`:

### Editar o arquivo de senhas
```bash
vigr /etc/passwd
```

### Editar o arquivo de grupos
```bash
vigr /etc/group
```

### Usar um editor específico
```bash
vigr -o nano /etc/sudoers
```

### Editar o arquivo de configuração em modo seguro
```bash
vigr -s /etc/fstab
```

## Tips
- Sempre use `vigr` para editar arquivos de configuração críticos, pois ele ajuda a prevenir erros de edição simultânea.
- Familiarize-se com o editor que você está usando (como `vi` ou `nano`) para facilitar a edição.
- Faça backup dos arquivos de configuração antes de editá-los, especialmente se você não estiver seguro sobre as alterações que está fazendo.