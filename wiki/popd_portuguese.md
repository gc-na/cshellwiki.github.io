# [Linux] Bash popd Uso: Remove diretórios da pilha

## Overview
O comando `popd` é utilizado para remover diretórios da pilha de diretórios em um ambiente de shell Bash. Ele permite que você retorne rapidamente ao diretório anterior que foi armazenado na pilha, facilitando a navegação entre diferentes diretórios.

## Usage
A sintaxe básica do comando `popd` é a seguinte:

```bash
popd [options] [arguments]
```

## Common Options
- `-n`: Não altera o diretório atual, apenas remove o diretório do topo da pilha.
- `+n`: Remove o diretório na posição `n` da pilha, onde `n` é um número que representa a posição do diretório.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `popd`:

1. **Remover o diretório do topo da pilha:**
   ```bash
   popd
   ```

2. **Remover o diretório na segunda posição da pilha:**
   ```bash
   popd +1
   ```

3. **Remover o diretório do topo da pilha sem mudar o diretório atual:**
   ```bash
   popd -n
   ```

4. **Adicionar diretórios à pilha e depois usar popd:**
   ```bash
   pushd /home/user/Documents
   pushd /home/user/Downloads
   popd  # Retorna para /home/user/Documents
   ```

## Tips
- Utilize `pushd` antes de `popd` para gerenciar sua pilha de diretórios de forma eficiente.
- Verifique o estado atual da pilha de diretórios usando o comando `dirs` antes de usar `popd`.
- Lembre-se de que o `popd` sempre remove o diretório do topo da pilha, então tenha cuidado ao usá-lo se você precisar de um diretório específico.