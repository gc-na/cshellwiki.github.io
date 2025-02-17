# [Linux] Bash lsblk Uso: Exibir informações sobre dispositivos de bloco

## Overview
O comando `lsblk` é utilizado para listar informações sobre todos os dispositivos de bloco disponíveis no sistema, como discos rígidos, partições e dispositivos removíveis. Ele exibe a hierarquia dos dispositivos e suas respectivas características, facilitando a visualização da estrutura de armazenamento.

## Usage
A sintaxe básica do comando `lsblk` é a seguinte:

```bash
lsblk [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `lsblk`:

- `-a` ou `--all`: Exibe todos os dispositivos, incluindo aqueles que não estão montados.
- `-f` ou `--fs`: Mostra informações sobre o sistema de arquivos, incluindo tipo e UUID.
- `-l` ou `--list`: Exibe a saída em formato de lista em vez de árvore.
- `-o` ou `--output`: Permite especificar quais colunas exibir na saída.
- `-n` ou `--noheadings`: Remove os cabeçalhos da saída.

## Common Examples

Aqui estão alguns exemplos práticos do uso do comando `lsblk`:

1. **Listar todos os dispositivos de bloco:**
   ```bash
   lsblk
   ```

2. **Listar todos os dispositivos, incluindo não montados:**
   ```bash
   lsblk -a
   ```

3. **Exibir informações do sistema de arquivos:**
   ```bash
   lsblk -f
   ```

4. **Listar dispositivos em formato de lista:**
   ```bash
   lsblk -l
   ```

5. **Especificar colunas a serem exibidas:**
   ```bash
   lsblk -o NAME,SIZE,TYPE,MOUNTPOINT
   ```

6. **Remover cabeçalhos da saída:**
   ```bash
   lsblk -n
   ```

## Tips
- Utilize a opção `-f` para obter informações detalhadas sobre sistemas de arquivos, o que pode ser útil ao gerenciar partições.
- Combine `lsblk` com outros comandos, como `grep`, para filtrar a saída e encontrar dispositivos específicos.
- Use `lsblk` em scripts para automatizar tarefas relacionadas à gestão de armazenamento, garantindo que você tenha sempre uma visão clara dos dispositivos disponíveis.