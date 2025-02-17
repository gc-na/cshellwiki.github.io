# [Linux] Bash dirname Uso: Extrair o diretório de um caminho

## Overview
O comando `dirname` é utilizado para extrair o diretório de um caminho de arquivo fornecido. Ele remove o nome do arquivo e retorna apenas a parte do diretório, facilitando a manipulação de caminhos em scripts e comandos.

## Usage
A sintaxe básica do comando `dirname` é a seguinte:

```bash
dirname [opções] [argumentos]
```

## Common Options
- `-z`: Trata os argumentos como uma lista de caminhos separados por nulo.
- `--help`: Exibe uma mensagem de ajuda com informações sobre o uso do comando.
- `--version`: Mostra a versão do comando `dirname`.

## Common Examples

Aqui estão alguns exemplos práticos do uso do comando `dirname`:

1. **Extrair o diretório de um caminho absoluto:**
   ```bash
   dirname /home/usuario/documentos/arquivo.txt
   ```
   Saída:
   ```
   /home/usuario/documentos
   ```

2. **Extrair o diretório de um caminho relativo:**
   ```bash
   dirname ./imagens/foto.jpg
   ```
   Saída:
   ```
   ./imagens
   ```

3. **Usar dirname em um caminho com múltiplos níveis:**
   ```bash
   dirname /var/log/syslog
   ```
   Saída:
   ```
   /var/log
   ```

4. **Combinar dirname com outros comandos:**
   ```bash
   echo $(dirname /usr/local/bin/script.sh)
   ```
   Saída:
   ```
   /usr/local/bin
   ```

## Tips
- Utilize `dirname` em scripts para manipular caminhos de arquivos de forma eficiente.
- Combine `dirname` com outros comandos, como `basename`, para obter tanto o diretório quanto o nome do arquivo em um único fluxo de trabalho.
- Lembre-se de que `dirname` não altera o sistema de arquivos; ele apenas fornece a parte do diretório do caminho especificado.