# [Linux] Bash cp Uso: Copiar arquivos e diretórios

## Overview
O comando `cp` é utilizado no Bash para copiar arquivos e diretórios de um local para outro. É uma ferramenta essencial para gerenciar e organizar dados no sistema.

## Usage
A sintaxe básica do comando `cp` é a seguinte:

```bash
cp [opções] [origem] [destino]
```

## Common Options
Aqui estão algumas opções comuns do comando `cp`:

- `-r`: Copia diretórios de forma recursiva.
- `-i`: Solicita confirmação antes de sobrescrever arquivos existentes.
- `-u`: Copia apenas arquivos que são mais novos que os arquivos de destino ou que não existem no destino.
- `-v`: Mostra o progresso da cópia, exibindo os arquivos à medida que são copiados.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `cp`:

1. **Copiar um arquivo para outro diretório:**
   ```bash
   cp arquivo.txt /caminho/para/diretorio/
   ```

2. **Copiar um diretório e seu conteúdo:**
   ```bash
   cp -r /caminho/para/diretorio_origem /caminho/para/diretorio_destino
   ```

3. **Copiar um arquivo e solicitar confirmação antes de sobrescrever:**
   ```bash
   cp -i arquivo.txt /caminho/para/diretorio/
   ```

4. **Copiar apenas arquivos mais novos:**
   ```bash
   cp -u arquivo.txt /caminho/para/diretorio/
   ```

5. **Copiar um arquivo e mostrar o progresso:**
   ```bash
   cp -v arquivo.txt /caminho/para/diretorio/
   ```

## Tips
- Sempre verifique o caminho de destino para evitar sobrescrever arquivos importantes.
- Use a opção `-i` para evitar perdas acidentais de dados.
- Para cópias de grandes diretórios, considere usar `rsync` para mais opções de controle e eficiência.