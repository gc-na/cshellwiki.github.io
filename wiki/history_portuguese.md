# [Linux] Bash history uso: Visualizar e gerenciar comandos executados

## Overview
O comando `history` no Bash é utilizado para exibir uma lista dos comandos que foram executados na sessão atual do terminal. Essa funcionalidade é útil para relembrar comandos anteriores e reutilizá-los sem precisar digitá-los novamente.

## Usage
A sintaxe básica do comando `history` é a seguinte:

```bash
history [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do comando `history`:

- `-c`: Limpa o histórico de comandos.
- `-d N`: Remove o comando na posição N do histórico.
- `N`: Exibe os últimos N comandos do histórico.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `history`:

1. **Exibir todo o histórico de comandos:**

   ```bash
   history
   ```

2. **Exibir os últimos 10 comandos:**

   ```bash
   history 10
   ```

3. **Limpar o histórico de comandos:**

   ```bash
   history -c
   ```

4. **Remover um comando específico do histórico (por exemplo, o comando na posição 5):**

   ```bash
   history -d 5
   ```

5. **Reexecutar um comando do histórico usando o número do comando (por exemplo, 42):**

   ```bash
   !42
   ```

## Tips
- Utilize o comando `!!` para repetir o último comando executado rapidamente.
- Para buscar um comando anterior, você pode usar `Ctrl + R` e começar a digitar parte do comando.
- Considere limpar o histórico periodicamente para manter a privacidade e evitar confusões com comandos antigos.