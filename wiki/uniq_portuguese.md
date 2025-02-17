# [Linux] Bash uniq Uso: Remove duplicatas de linhas em um arquivo

## Overview
O comando `uniq` é utilizado para filtrar linhas duplicadas em um arquivo ou na entrada padrão. Ele é frequentemente usado em conjunto com o comando `sort`, pois `uniq` apenas remove duplicatas que estão adjacentes.

## Usage
A sintaxe básica do comando `uniq` é a seguinte:

```bash
uniq [opções] [arquivo]
```

## Common Options
Aqui estão algumas opções comuns do comando `uniq`:

- `-c`: Conta o número de ocorrências de cada linha.
- `-d`: Exibe apenas as linhas que aparecem mais de uma vez.
- `-u`: Exibe apenas as linhas que aparecem uma única vez.
- `-i`: Ignora diferenças entre maiúsculas e minúsculas ao comparar linhas.

## Common Examples

### Exemplo 1: Remover duplicatas de um arquivo
Para remover linhas duplicadas de um arquivo chamado `exemplo.txt`:

```bash
uniq exemplo.txt
```

### Exemplo 2: Contar ocorrências de cada linha
Para contar quantas vezes cada linha aparece em `exemplo.txt`:

```bash
uniq -c exemplo.txt
```

### Exemplo 3: Exibir apenas linhas duplicadas
Para mostrar apenas as linhas que aparecem mais de uma vez:

```bash
uniq -d exemplo.txt
```

### Exemplo 4: Ignorar maiúsculas e minúsculas
Para remover duplicatas ignorando diferenças de caixa:

```bash
uniq -i exemplo.txt
```

## Tips
- Sempre use `sort` antes de `uniq` se você não tiver certeza de que as linhas duplicadas estão adjacentes. Por exemplo:
  
  ```bash
  sort exemplo.txt | uniq
  ```

- Combine `-c` com `sort -n` para listar linhas duplicadas em ordem numérica de frequência:

  ```bash
  sort exemplo.txt | uniq -c | sort -n
  ```

- Lembre-se de que `uniq` não altera o arquivo original; ele apenas exibe a saída no terminal. Para salvar a saída em um novo arquivo, redirecione a saída:

  ```bash
  uniq exemplo.txt > resultado.txt
  ```