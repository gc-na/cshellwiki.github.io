# [Linux] Bash if: Avalia condições

## Overview
O comando `if` no Bash é utilizado para executar comandos com base na avaliação de condições. Ele permite que você execute diferentes blocos de código dependendo se uma condição é verdadeira ou falsa.

## Usage
A sintaxe básica do comando `if` é a seguinte:

```bash
if [ condição ]; then
    # comandos a serem executados se a condição for verdadeira
else
    # comandos a serem executados se a condição for falsa
fi
```

## Common Options
- `-e`: Verifica se um arquivo existe.
- `-d`: Verifica se um diretório existe.
- `-f`: Verifica se um arquivo é um arquivo regular.
- `-z`: Verifica se a string é vazia.
- `-n`: Verifica se a string não é vazia.

## Common Examples

### Exemplo 1: Verificar se um arquivo existe
```bash
if [ -e "meuarquivo.txt" ]; then
    echo "O arquivo existe."
else
    echo "O arquivo não existe."
fi
```

### Exemplo 2: Verificar se uma variável está vazia
```bash
variavel=""
if [ -z "$variavel" ]; then
    echo "A variável está vazia."
else
    echo "A variável não está vazia."
fi
```

### Exemplo 3: Comparar números
```bash
numero1=10
numero2=20
if [ $numero1 -lt $numero2 ]; then
    echo "$numero1 é menor que $numero2."
else
    echo "$numero1 não é menor que $numero2."
fi
```

### Exemplo 4: Verificar se um diretório existe
```bash
if [ -d "/home/usuario/pasta" ]; then
    echo "O diretório existe."
else
    echo "O diretório não existe."
fi
```

## Tips
- Sempre use espaços ao redor dos colchetes `[` e `]` para evitar erros de sintaxe.
- Utilize `elif` para adicionar múltiplas condições.
- Para evitar problemas com variáveis não definidas, sempre coloque as variáveis entre aspas.
- Teste suas condições em um terminal antes de incorporá-las em scripts mais complexos.