# [Linux] Bash w: Exibir usuários conectados e suas atividades

## Overview
O comando `w` é utilizado para exibir informações sobre os usuários que estão atualmente conectados ao sistema, bem como suas atividades. Ele fornece detalhes como o tempo de atividade do sistema, o tempo que cada usuário está logado e o que cada um está fazendo no momento.

## Usage
A sintaxe básica do comando `w` é a seguinte:

```bash
w [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do comando `w`:

- `-h`: Remove o cabeçalho da saída.
- `-s`: Exibe uma saída mais compacta, omitindo algumas informações.
- `-u`: Exibe o nome do usuário em vez do ID do usuário.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `w`:

1. **Exibir todos os usuários conectados:**
   ```bash
   w
   ```

2. **Exibir informações sem o cabeçalho:**
   ```bash
   w -h
   ```

3. **Exibir informações de forma compacta:**
   ```bash
   w -s
   ```

4. **Exibir informações com o nome do usuário:**
   ```bash
   w -u
   ```

## Tips
- Utilize o comando `w` regularmente para monitorar a atividade dos usuários em sistemas multiusuário.
- Combine o `w` com outros comandos, como `grep`, para filtrar informações específicas sobre usuários.
- Lembre-se de que a saída do `w` pode variar dependendo das permissões do usuário que executa o comando.