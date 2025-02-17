# [Linux] Bash du Uso: Exibe o uso de espaço em disco

## Overview
O comando `du` (disk usage) é utilizado para estimar e relatar o espaço em disco utilizado por arquivos e diretórios no sistema de arquivos. Ele é uma ferramenta útil para monitorar o uso de espaço e identificar quais arquivos ou pastas estão ocupando mais espaço.

## Usage
A sintaxe básica do comando `du` é a seguinte:

```bash
du [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do comando `du`:

- `-h`: Exibe os tamanhos em um formato legível por humanos (por exemplo, KB, MB).
- `-s`: Mostra apenas o total para cada argumento, sem listar os subdiretórios.
- `-a`: Inclui arquivos individuais na saída, além de diretórios.
- `-c`: Exibe um total cumulativo no final da saída.
- `--max-depth=N`: Limita a profundidade da listagem de diretórios a N níveis.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `du`:

1. **Ver o uso de espaço em disco de um diretório específico:**
   ```bash
   du /caminho/para/diretorio
   ```

2. **Ver o uso de espaço em disco de um diretório com tamanhos legíveis por humanos:**
   ```bash
   du -h /caminho/para/diretorio
   ```

3. **Obter apenas o total de espaço utilizado por um diretório:**
   ```bash
   du -sh /caminho/para/diretorio
   ```

4. **Listar o uso de espaço de todos os arquivos e diretórios no diretório atual:**
   ```bash
   du -ah
   ```

5. **Limitar a profundidade da listagem a 1 nível:**
   ```bash
   du --max-depth=1 -h
   ```

## Tips
- Utilize a opção `-h` para facilitar a leitura dos tamanhos, especialmente em diretórios grandes.
- Combine `du` com `sort` para ordenar os resultados por tamanho, por exemplo:
  ```bash
  du -h | sort -hr
  ```
- Use `du -c` para obter um total geral do uso de espaço ao final da listagem, o que pode ser útil para relatórios.
- Para uma análise mais detalhada, considere usar `du` em conjunto com outros comandos, como `grep`, para filtrar resultados específicos.