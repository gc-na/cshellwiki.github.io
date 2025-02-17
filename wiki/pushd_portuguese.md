# [Linux] Bash pushd Uso: Gerenciar diretórios na pilha

## Overview
O comando `pushd` é utilizado para gerenciar diretórios em uma pilha, permitindo que você navegue rapidamente entre diferentes diretórios no terminal. Ele adiciona o diretório atual à pilha e muda para o diretório especificado, facilitando a navegação.

## Usage
A sintaxe básica do comando `pushd` é a seguinte:

```bash
pushd [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns para o comando `pushd`:

- `+n`: Muda para o diretório na posição `n` da pilha.
- `-n`: Muda para o diretório na posição `n` da pilha, mas não o remove da pilha.
- `--help`: Exibe a ajuda do comando.

## Common Examples

1. **Adicionar um diretório à pilha e mudar para ele:**
   ```bash
   pushd /caminho/para/diretorio
   ```

2. **Voltar ao diretório anterior na pilha:**
   ```bash
   pushd -
   ```

3. **Listar os diretórios na pilha:**
   ```bash
   dirs
   ```

4. **Mudar para o segundo diretório na pilha:**
   ```bash
   pushd +1
   ```

5. **Mudar para o terceiro diretório na pilha sem removê-lo:**
   ```bash
   pushd -3
   ```

## Tips
- Utilize `dirs` frequentemente para visualizar a pilha de diretórios e saber onde você está.
- Combine `pushd` com `popd` para alternar entre diretórios de forma eficiente.
- Lembre-se de que a pilha de diretórios é limitada à sessão do terminal, então, ao fechar o terminal, a pilha será perdida.