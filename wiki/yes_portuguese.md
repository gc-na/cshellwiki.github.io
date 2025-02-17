# [Linux] Bash yes uso equivalente: Gera uma sequência de respostas "yes"

## Overview
O comando `yes` é uma ferramenta simples que gera uma sequência contínua da palavra "yes" ou de qualquer outra string especificada. Ele é frequentemente utilizado em scripts para automatizar respostas afirmativas em comandos que requerem confirmação.

## Usage
A sintaxe básica do comando `yes` é a seguinte:

```bash
yes [opções] [argumentos]
```

Se nenhum argumento for fornecido, o comando irá gerar repetidamente a palavra "yes".

## Common Options
- `-n`: Não imprime a nova linha após cada repetição. Útil quando se deseja uma saída contínua em uma única linha.
- `--help`: Exibe uma mensagem de ajuda com informações sobre o uso do comando.
- `--version`: Mostra a versão do comando `yes`.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `yes`:

1. **Gerar repetidamente a palavra "yes":**
   ```bash
   yes
   ```

2. **Gerar uma sequência de uma string personalizada:**
   ```bash
   yes "Estou pronto!"
   ```

3. **Usar `yes` para confirmar um comando que requer múltiplas confirmações:**
   ```bash
   yes | rm -i *.txt
   ```
   Neste exemplo, `yes` envia respostas afirmativas para o comando `rm`, que pede confirmação para excluir arquivos `.txt`.

4. **Imprimir "yes" sem nova linha:**
   ```bash
   yes -n "Sim" | head -n 5
   ```
   Isso irá imprimir "Sim" cinco vezes na mesma linha.

## Tips
- Use o comando `yes` com cuidado, especialmente em scripts, pois ele pode causar a execução de ações indesejadas se não for controlado adequadamente.
- Combine `yes` com outros comandos que exigem confirmação para automatizar tarefas repetitivas.
- Teste o comando em um ambiente seguro antes de usá-lo em produção para evitar perda de dados acidental.