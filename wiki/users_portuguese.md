# [Linux] Usuários Bash: Exibir informações sobre usuários do sistema

## Overview
O comando `users` é utilizado para exibir os nomes dos usuários que estão atualmente logados no sistema. Ele fornece uma visão rápida de quem está ativo no momento.

## Usage
A sintaxe básica do comando é a seguinte:

```
users [opções]
```

## Common Options
- `-a`: Exibe todos os nomes de usuários, incluindo aqueles que estão logados em sessões de terminal diferentes.
- `-r`: Exibe apenas os usuários que estão logados em sessões de terminal reais.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `users`:

1. **Exibir usuários logados atualmente:**
   ```bash
   users
   ```

2. **Exibir todos os usuários logados, incluindo sessões de terminal diferentes:**
   ```bash
   users -a
   ```

3. **Exibir apenas usuários em sessões de terminal reais:**
   ```bash
   users -r
   ```

## Tips
- Utilize o comando `who` para obter informações mais detalhadas sobre os usuários logados, como o horário de login e o terminal utilizado.
- Combine o comando `users` com outros comandos, como `sort`, para organizar a saída de forma mais útil. Por exemplo:
  ```bash
  users | sort | uniq
  ```
- O comando `users` é útil para scripts de monitoramento, onde você pode querer verificar rapidamente quem está ativo no sistema.