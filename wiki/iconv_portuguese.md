# [Linux] Bash iconv Uso: Conversão de codificações de texto

## Overview
O comando `iconv` é utilizado para converter a codificação de arquivos de texto. Ele permite que você mude a forma como os caracteres são representados, o que é especialmente útil ao lidar com arquivos que podem ter sido criados em diferentes sistemas ou com diferentes configurações de codificação.

## Usage
A sintaxe básica do comando `iconv` é a seguinte:

```bash
iconv [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `iconv`:

- `-f` : Especifica a codificação de origem.
- `-t` : Especifica a codificação de destino.
- `-o` : Define o nome do arquivo de saída.
- `-c` : Ignora caracteres inválidos durante a conversão.

## Common Examples

### Exemplo 1: Converter de UTF-8 para ISO-8859-1
```bash
iconv -f UTF-8 -t ISO-8859-1 arquivo_entrada.txt -o arquivo_saida.txt
```

### Exemplo 2: Converter de Windows-1252 para UTF-8
```bash
iconv -f WINDOWS-1252 -t UTF-8 arquivo_entrada.txt -o arquivo_saida.txt
```

### Exemplo 3: Ignorar caracteres inválidos
```bash
iconv -f UTF-8 -t ISO-8859-1 -c arquivo_entrada.txt -o arquivo_saida.txt
```

### Exemplo 4: Converter e exibir no terminal
```bash
iconv -f UTF-8 -t ISO-8859-1 arquivo_entrada.txt
```

## Tips
- Sempre verifique a codificação do arquivo de entrada antes de usar o `iconv` para evitar erros de conversão.
- Utilize a opção `-c` para ignorar caracteres que não podem ser convertidos, evitando que o comando falhe.
- Teste a conversão em um arquivo de exemplo antes de aplicá-la em arquivos importantes, para garantir que o resultado seja o esperado.