# [Linux] Bash vgs Uso: Exibir informações sobre grupos de volumes

## Overview
O comando `vgs` é utilizado para exibir informações sobre grupos de volumes no Linux. Ele faz parte do sistema de gerenciamento de volumes lógicos (LVM) e fornece detalhes sobre os grupos de volumes, como tamanho, espaço livre e atributos.

## Usage
A sintaxe básica do comando `vgs` é a seguinte:

```bash
vgs [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `vgs`:

- `-o, --units`: Especifica as unidades de medida a serem usadas na saída.
- `--noheadings`: Remove os cabeçalhos da saída.
- `-a, --all`: Exibe todos os grupos de volumes, incluindo os inativos.
- `-h, --help`: Mostra a ajuda sobre o comando e suas opções.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `vgs`:

1. **Exibir informações básicas sobre grupos de volumes:**
   ```bash
   vgs
   ```

2. **Exibir informações detalhadas com unidades:**
   ```bash
   vgs -o +pv_count,lv_count
   ```

3. **Exibir todos os grupos de volumes, incluindo os inativos:**
   ```bash
   vgs -a
   ```

4. **Remover cabeçalhos da saída:**
   ```bash
   vgs --noheadings
   ```

## Tips
- Utilize a opção `-o` para personalizar quais informações deseja ver na saída, tornando-a mais relevante para suas necessidades.
- Combine o comando `vgs` com outros comandos LVM, como `lvdisplay` e `pvdisplay`, para obter uma visão completa do seu sistema de armazenamento.
- Verifique regularmente os grupos de volumes para monitorar o espaço disponível e evitar problemas de armazenamento no futuro.