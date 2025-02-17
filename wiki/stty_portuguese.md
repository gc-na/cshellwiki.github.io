# [Linux] Bash stty Uso: Configuração de terminal

## Overview
O comando `stty` é utilizado para modificar e exibir as configurações do terminal. Ele permite que os usuários ajustem comportamentos como a entrada e saída de dados, controle de fluxo e outros aspectos do terminal.

## Usage
A sintaxe básica do comando `stty` é a seguinte:

```bash
stty [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `stty`:

- `-a`: Exibe todas as configurações atuais do terminal.
- `-g`: Exibe as configurações atuais em um formato que pode ser usado para restaurá-las mais tarde.
- `erase`: Define o caractere usado para apagar o último caractere digitado.
- `kill`: Define o caractere que apaga toda a linha de entrada.
- `intr`: Define o caractere usado para interromper um processo em execução.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `stty`:

1. **Exibir configurações atuais do terminal:**
   ```bash
   stty -a
   ```

2. **Definir o caractere de apagar como Ctrl+H:**
   ```bash
   stty erase ^H
   ```

3. **Definir o caractere de matar a linha como Ctrl+U:**
   ```bash
   stty kill ^U
   ```

4. **Salvar as configurações atuais em uma variável:**
   ```bash
   settings=$(stty -g)
   ```

5. **Restaurar as configurações a partir da variável salva:**
   ```bash
   stty $settings
   ```

## Tips
- Sempre verifique as configurações atuais do terminal antes de fazer alterações, usando `stty -a`.
- Use `stty -g` para salvar as configurações antes de modificá-las, permitindo que você possa restaurá-las facilmente.
- Lembre-se de que algumas configurações podem afetar o comportamento de outros programas que você executa no terminal.