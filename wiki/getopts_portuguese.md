# [Linux] Bash getopts Uso: Processar opções de linha de comando

## Overview
O comando `getopts` é utilizado em scripts Bash para analisar opções de linha de comando. Ele permite que você defina opções que podem ser passadas para o seu script, facilitando a personalização do comportamento do script com base nas entradas do usuário.

## Usage
A sintaxe básica do comando `getopts` é a seguinte:

```bash
getopts [options] [arguments]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com `getopts`:

- `-a`: Ativa a opção 'a'.
- `-b`: Ativa a opção 'b'.
- `-c`: Ativa a opção 'c'.
- `:`: Indica que a opção requer um argumento.

## Common Examples

### Exemplo 1: Opções simples
```bash
#!/bin/bash

while getopts "ab:c:" opt; do
  case $opt in
    a)
      echo "Opção -a ativada"
      ;;
    b)
      echo "Opção -b ativada com argumento: $OPTARG"
      ;;
    c)
      echo "Opção -c ativada com argumento: $OPTARG"
      ;;
    *)
      echo "Opção inválida"
      ;;
  esac
done
```

### Exemplo 2: Usando o script
```bash
./meuscript.sh -a -b valor1 -c valor2
```
Saída:
```
Opção -a ativada
Opção -b ativada com argumento: valor1
Opção -c ativada com argumento: valor2
```

### Exemplo 3: Tratamento de erro
```bash
#!/bin/bash

while getopts "a:b:" opt; do
  case $opt in
    a)
      echo "Opção -a ativada"
      ;;
    b)
      echo "Opção -b ativada com argumento: $OPTARG"
      ;;
    *)
      echo "Uso: $0 [-a] [-b valor]"
      exit 1
      ;;
  esac
done
```

## Tips
- Sempre inclua um caso `*` no seu `case` para capturar opções inválidas.
- Use dois pontos (`:`) após uma opção para indicar que ela requer um argumento.
- Teste seu script com diferentes combinações de opções para garantir que ele funcione conforme o esperado.