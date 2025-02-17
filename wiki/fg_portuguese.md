# [Linux] Bash fg Uso equivalente: Colocar um trabalho em primeiro plano

O comando `fg` é utilizado para trazer um trabalho em segundo plano para o primeiro plano no terminal.

## Overview
O comando `fg` (foreground) é uma ferramenta útil no Bash que permite ao usuário retomar um processo que foi suspenso ou enviado para o segundo plano, trazendo-o de volta para o primeiro plano. Isso é especialmente útil quando você precisa interagir com um processo que estava em execução anteriormente.

## Usage
A sintaxe básica do comando `fg` é a seguinte:

```bash
fg [opções] [número do trabalho]
```

## Common Options
- **%n**: Especifica o número do trabalho que você deseja trazer para o primeiro plano. O número pode ser obtido usando o comando `jobs`.
- **%job_id**: Permite referenciar um trabalho pelo seu ID. Por exemplo, `%1` para o primeiro trabalho.

## Common Examples

1. **Trazer o último trabalho em segundo plano para o primeiro plano:**
   ```bash
   fg
   ```

2. **Trazer um trabalho específico (por exemplo, o trabalho 2) para o primeiro plano:**
   ```bash
   fg %2
   ```

3. **Trazer um trabalho usando seu ID:**
   ```bash
   fg %1
   ```

4. **Se você tiver vários trabalhos, pode listar todos eles com:**
   ```bash
   jobs
   ```

## Tips
- Sempre verifique a lista de trabalhos em segundo plano usando `jobs` antes de usar `fg`, para saber qual trabalho você deseja trazer para o primeiro plano.
- Se você precisar suspender um trabalho em primeiro plano, use `Ctrl + Z` antes de usar `fg` para trazê-lo de volta.
- Lembre-se de que apenas um trabalho pode estar em primeiro plano por vez, então, se você já tiver um trabalho em primeiro plano, precisará suspender ou finalizar esse trabalho antes de usar `fg` novamente.