# [Linux] Bash id uso: exibir informações de identificação do usuário

## Overview
O comando `id` no Bash é utilizado para exibir informações sobre a identidade do usuário atual ou de um usuário específico. Ele fornece detalhes como o UID (User ID), GID (Group ID) e os grupos aos quais o usuário pertence.

## Usage
A sintaxe básica do comando `id` é a seguinte:

```bash
id [opções] [argumentos]
```

## Common Options
- `-u`: Exibe apenas o UID do usuário.
- `-g`: Exibe apenas o GID do grupo primário do usuário.
- `-G`: Exibe todos os GIDs dos grupos aos quais o usuário pertence.
- `-n`: Exibe o nome do usuário ou grupo em vez do número correspondente.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `id`:

1. **Exibir informações do usuário atual:**
   ```bash
   id
   ```

2. **Exibir o UID do usuário atual:**
   ```bash
   id -u
   ```

3. **Exibir o GID do grupo primário do usuário atual:**
   ```bash
   id -g
   ```

4. **Exibir todos os GIDs dos grupos do usuário atual:**
   ```bash
   id -G
   ```

5. **Exibir informações de um usuário específico:**
   ```bash
   id nome_do_usuario
   ```

6. **Exibir o nome do usuário em vez do UID:**
   ```bash
   id -n -u
   ```

## Tips
- Utilize `id` sem opções para obter uma visão geral rápida das informações do usuário.
- Combine as opções para obter informações específicas de forma mais eficiente.
- O comando `id` é útil para scripts que precisam verificar permissões ou grupos de usuários.