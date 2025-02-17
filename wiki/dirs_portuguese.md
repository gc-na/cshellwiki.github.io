# [Linux] Bash dirs Uso: Exibir diretórios na pilha

## Overview
O comando `dirs` é utilizado no Bash para exibir a lista de diretórios que estão na pilha de diretórios. Essa pilha é manipulada por comandos como `pushd` e `popd`, permitindo que os usuários naveguem facilmente entre diferentes diretórios.

## Usage
A sintaxe básica do comando `dirs` é a seguinte:

```bash
dirs [options] [arguments]
```

## Common Options
- `-l`: Exibe os diretórios em formato longo, mostrando o caminho completo.
- `-p`: Exibe os diretórios em formato de pilha, sem espaços adicionais.

## Common Examples

1. **Exibir a pilha de diretórios atual**:
   ```bash
   dirs
   ```

2. **Exibir a pilha de diretórios em formato longo**:
   ```bash
   dirs -l
   ```

3. **Exibir a pilha de diretórios sem espaços**:
   ```bash
   dirs -p
   ```

4. **Adicionar um diretório à pilha e exibir**:
   ```bash
   pushd /home/user
   dirs
   ```

5. **Remover o diretório do topo da pilha e exibir**:
   ```bash
   popd
   dirs
   ```

## Tips
- Utilize `pushd` e `popd` em conjunto com `dirs` para gerenciar sua navegação de diretórios de forma eficiente.
- Lembre-se de que a pilha de diretórios é uma ferramenta poderosa para alternar rapidamente entre locais de trabalho sem precisar digitar caminhos longos repetidamente.
- Experimente usar `dirs -l` para ter uma visão mais clara dos diretórios em sua pilha, especialmente se você estiver trabalhando com caminhos longos.