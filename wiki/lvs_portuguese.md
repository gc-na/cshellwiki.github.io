# [Linux] Bash lvs Uso: Exibir informações sobre volumes lógicos

## Overview
O comando `lvs` é utilizado para exibir informações sobre volumes lógicos em sistemas que utilizam o LVM (Logical Volume Manager). Ele fornece uma visão geral dos volumes lógicos disponíveis, incluindo detalhes como tamanho, atributos e status.

## Usage
A sintaxe básica do comando `lvs` é a seguinte:

```bash
lvs [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `lvs`:

- `-o, --units`: Especifica as unidades de medida a serem usadas na saída.
- `-a, --all`: Exibe todos os volumes lógicos, incluindo aqueles que estão inativos.
- `-h, --help`: Mostra a ajuda sobre o comando e suas opções.
- `-o, --options`: Permite selecionar quais colunas exibir na saída.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `lvs`:

1. **Exibir todos os volumes lógicos:**
   ```bash
   lvs
   ```

2. **Exibir todos os volumes lógicos, incluindo os inativos:**
   ```bash
   lvs -a
   ```

3. **Exibir volumes lógicos com unidades legíveis:**
   ```bash
   lvs -o +devices --units m
   ```

4. **Mostrar ajuda sobre o comando:**
   ```bash
   lvs --help
   ```

## Tips
- Sempre verifique se você tem permissões adequadas para visualizar os volumes lógicos, especialmente em sistemas multiusuário.
- Use a opção `--units` para facilitar a leitura dos tamanhos dos volumes, especialmente em sistemas com muitos dados.
- Combine o `lvs` com outros comandos do LVM, como `lvcreate` ou `lvremove`, para gerenciar volumes lógicos de forma mais eficaz.