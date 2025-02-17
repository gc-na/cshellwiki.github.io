# [Linux] Bash mv Uso: Mover ou renomear arquivos e diretórios

## Overview
O comando `mv` é utilizado no Bash para mover ou renomear arquivos e diretórios. Ele é uma ferramenta essencial para a organização de arquivos no sistema de arquivos.

## Usage
A sintaxe básica do comando `mv` é a seguinte:

```bash
mv [opções] [origem] [destino]
```

## Common Options
Aqui estão algumas opções comuns do comando `mv`:

- `-i`: Pergunta antes de sobrescrever um arquivo existente.
- `-u`: Move apenas se o arquivo de origem for mais recente que o arquivo de destino ou se o arquivo de destino não existir.
- `-v`: Exibe uma mensagem detalhada sobre o que está sendo feito.
- `-f`: Força a movimentação, sobrescrevendo arquivos sem perguntar.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `mv`:

1. **Mover um arquivo para um diretório:**
   ```bash
   mv arquivo.txt /caminho/para/diretorio/
   ```

2. **Renomear um arquivo:**
   ```bash
   mv arquivo_antigo.txt arquivo_novo.txt
   ```

3. **Mover e renomear um arquivo ao mesmo tempo:**
   ```bash
   mv /caminho/para/arquivo.txt /novo/caminho/para/novo_nome.txt
   ```

4. **Mover um diretório:**
   ```bash
   mv /caminho/para/diretorio /novo/caminho/para/diretorio
   ```

5. **Usar a opção interativa para evitar sobrescrever:**
   ```bash
   mv -i arquivo.txt /caminho/para/diretorio/
   ```

## Tips
- Sempre use a opção `-i` se estiver movendo arquivos importantes, para evitar sobrescrever acidentalmente.
- Utilize a opção `-v` para visualizar o que está sendo movido, especialmente útil em operações com múltiplos arquivos.
- Verifique se o caminho de destino existe antes de mover arquivos, para evitar confusões.