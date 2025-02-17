# [Linux] Bash @ Uso: Executar comandos em segundo plano

## Overview
O comando `@` no Bash é utilizado para executar comandos em segundo plano, permitindo que o usuário continue utilizando o terminal enquanto o comando é processado.

## Usage
A sintaxe básica do comando é a seguinte:

```bash
@ [opções] [argumentos]
```

## Common Options
- `&`: Coloca o comando em segundo plano.
- `disown`: Remove o comando da lista de jobs do shell, permitindo que ele continue executando mesmo após o fechamento do terminal.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `@`:

1. Executar um script em segundo plano:
   ```bash
   ./meu_script.sh &
   ```

2. Executar um comando de longa duração em segundo plano:
   ```bash
   sleep 100 &
   ```

3. Executar um comando e desassociá-lo do terminal:
   ```bash
   long_running_command & disown
   ```

4. Verificar os jobs em segundo plano:
   ```bash
   jobs
   ```

## Tips
- Sempre verifique os jobs em segundo plano com o comando `jobs` para monitorar o que está sendo executado.
- Use `fg` para trazer um job em segundo plano de volta para o primeiro plano, se necessário.
- Lembre-se de usar `disown` se você quiser que o comando continue executando mesmo após fechar o terminal.