# [Linux] Bash unset Uso: Remove variáveis e funções do ambiente

## Overview
O comando `unset` é utilizado no Bash para remover variáveis e funções do ambiente atual. Isso é útil quando você deseja limpar variáveis que não são mais necessárias ou evitar conflitos entre nomes de variáveis.

## Usage
A sintaxe básica do comando `unset` é a seguinte:

```bash
unset [opções] [argumentos]
```

## Common Options
- `-f`: Remove uma função do ambiente.
- `-v`: Remove uma variável do ambiente.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `unset`:

1. **Remover uma variável:**
   ```bash
   MY_VAR="Hello, World!"
   echo $MY_VAR  # Saída: Hello, World!
   unset MY_VAR
   echo $MY_VAR  # Saída: (nada)
   ```

2. **Remover uma função:**
   ```bash
   my_function() {
       echo "Esta é uma função."
   }
   my_function  # Saída: Esta é uma função.
   unset -f my_function
   my_function  # Saída: bash: my_function: command not found
   ```

3. **Remover múltiplas variáveis:**
   ```bash
   VAR1="Valor 1"
   VAR2="Valor 2"
   echo $VAR1 $VAR2  # Saída: Valor 1 Valor 2
   unset VAR1 VAR2
   echo $VAR1 $VAR2  # Saída: (nada) (nada)
   ```

## Tips
- Sempre verifique se a variável ou função que você está removendo não é necessária em outras partes do seu script.
- Use `unset -v` para garantir que você está removendo uma variável e não uma função, caso ambos tenham o mesmo nome.
- Após usar `unset`, você pode verificar se a variável foi realmente removida usando `echo` ou `declare -p`.