# [Linux] Bash rev: Inverte linhas de texto

## Overview
O comando `rev` é utilizado para inverter as linhas de texto de um arquivo ou da entrada padrão. Ele lê cada linha e a reverte, apresentando o resultado na saída padrão. É uma ferramenta simples, mas útil em várias situações de manipulação de texto.

## Usage
A sintaxe básica do comando `rev` é a seguinte:

```bash
rev [opções] [argumentos]
```

## Common Options
- `-o, --output=ARQUIVO`: Especifica um arquivo de saída para armazenar o resultado.
- `-h, --help`: Exibe uma mensagem de ajuda com informações sobre o uso do comando.
- `-V, --version`: Mostra a versão do comando `rev`.

## Common Examples

### Exemplo 1: Inverter uma linha de texto
Para inverter uma linha de texto diretamente do terminal, você pode usar:

```bash
echo "Olá Mundo" | rev
```
**Saída:**
```
odnuM alO
```

### Exemplo 2: Inverter linhas de um arquivo
Se você tiver um arquivo chamado `texto.txt` com várias linhas, pode inverter todas as linhas assim:

```bash
rev texto.txt
```

### Exemplo 3: Salvar a saída em um novo arquivo
Para inverter as linhas de um arquivo e salvar o resultado em um novo arquivo chamado `inverso.txt`, use:

```bash
rev texto.txt > inverso.txt
```

### Exemplo 4: Usar com redirecionamento
Você também pode usar o `rev` com redirecionamento de entrada:

```bash
rev < texto.txt
```

## Tips
- Utilize `rev` em conjunto com outros comandos, como `cat` ou `grep`, para manipulações mais complexas de texto.
- Lembre-se de que o `rev` inverte apenas as linhas, não altera a ordem das linhas no arquivo original.
- Para visualizar rapidamente o resultado, combine `rev` com `less` ou `more` para uma navegação mais fácil em arquivos grandes.