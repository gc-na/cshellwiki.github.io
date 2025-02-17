# [Linux] Bash parted Uso: Gerenciar partições de disco

## Overview
O comando `parted` é uma ferramenta poderosa utilizada para gerenciar partições de disco em sistemas Linux. Ele permite criar, excluir, redimensionar e modificar partições de forma eficiente, facilitando a administração do espaço em disco.

## Usage
A sintaxe básica do comando `parted` é a seguinte:

```bash
parted [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `parted`:

- `-l` ou `--list`: Lista todas as partições disponíveis.
- `mkpart`: Cria uma nova partição.
- `rm`: Remove uma partição existente.
- `resizepart`: Redimensiona uma partição existente.
- `print`: Exibe a tabela de partições atual.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `parted`:

1. **Listar todas as partições**:
   ```bash
   parted -l
   ```

2. **Criar uma nova partição**:
   ```bash
   parted /dev/sda mkpart primary ext4 1MiB 100MiB
   ```

3. **Remover uma partição**:
   ```bash
   parted /dev/sda rm 1
   ```

4. **Redimensionar uma partição**:
   ```bash
   parted /dev/sda resizepart 1 200MiB
   ```

5. **Exibir a tabela de partições**:
   ```bash
   parted /dev/sda print
   ```

## Tips
- Sempre faça backup dos dados importantes antes de modificar partições.
- Use o `print` para verificar a tabela de partições antes de realizar alterações.
- Para operações que exigem mais segurança, considere usar `parted` em modo interativo, iniciando-o apenas com `parted` e, em seguida, digitando os comandos desejados.