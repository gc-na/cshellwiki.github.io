# [Linux] Bash who uso equivalente: Exibir usuários conectados

## Overview
O comando `who` é utilizado para exibir uma lista de usuários que estão atualmente conectados ao sistema. Ele fornece informações como o nome do usuário, o terminal em que estão logados, a data e hora do login, entre outros detalhes.

## Usage
A sintaxe básica do comando `who` é a seguinte:

```bash
who [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do comando `who`:

- `-a`: Exibe todas as informações disponíveis, incluindo usuários conectados e informações sobre o sistema.
- `-b`: Mostra a última vez que o sistema foi inicializado.
- `-q`: Exibe apenas a lista de usuários conectados, sem informações adicionais.
- `--help`: Mostra uma ajuda rápida sobre o uso do comando.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `who`:

1. **Exibir todos os usuários conectados:**
   ```bash
   who
   ```

2. **Mostrar a última vez que o sistema foi inicializado:**
   ```bash
   who -b
   ```

3. **Listar apenas os nomes dos usuários conectados:**
   ```bash
   who -q
   ```

4. **Exibir todas as informações disponíveis:**
   ```bash
   who -a
   ```

## Tips
- Utilize `who -q` para obter uma visão rápida dos usuários conectados, especialmente em sistemas com muitos usuários.
- Combine o comando `who` com `wc -l` para contar quantos usuários estão logados:
  ```bash
  who | wc -l
  ```
- Para monitorar a atividade em tempo real, considere usar o comando `watch` junto com `who`:
  ```bash
  watch who
  ```