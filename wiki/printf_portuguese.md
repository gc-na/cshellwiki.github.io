# [Linux] Bash printf Uso: Formatação de saída de texto

## Overview
O comando `printf` no Bash é utilizado para formatar e imprimir texto na saída padrão. Ele é semelhante à função `printf` em linguagens de programação como C, permitindo que você controle a formatação de strings, números e outros tipos de dados.

## Usage
A sintaxe básica do comando `printf` é a seguinte:

```bash
printf [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `printf`:

- `-v nome`: Atribui a saída formatada a uma variável em vez de imprimi-la.
- `-f formato`: Especifica um formato de saída personalizado.
- `--help`: Mostra uma ajuda rápida sobre o uso do comando.

## Common Examples

### Exemplo 1: Impressão simples
Imprimindo uma string simples:
```bash
printf "Olá, Mundo!\n"
```

### Exemplo 2: Formatação de números
Formatando um número com duas casas decimais:
```bash
printf "O valor é: %.2f\n" 3.14159
```

### Exemplo 3: Impressão de múltiplos argumentos
Imprimindo múltiplos valores formatados:
```bash
printf "Nome: %s, Idade: %d\n" "Alice" 30
```

### Exemplo 4: Atribuindo a uma variável
Atribuindo a saída formatada a uma variável:
```bash
printf -v resultado "O valor é: %.2f" 2.71828
echo "$resultado"
```

## Tips
- Utilize `%s` para strings e `%d` para inteiros ao formatar saídas.
- Lembre-se de incluir `\n` no final da string para garantir que a saída seja exibida em uma nova linha.
- Teste diferentes especificadores de formato para obter a saída desejada, como `%x` para hexadecimal ou `%c` para caracteres.