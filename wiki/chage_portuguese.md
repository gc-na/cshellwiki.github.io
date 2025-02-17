# [Linux] Bash chage Uso: Gerenciar a expiração de senhas de usuários

## Overview
O comando `chage` é utilizado para modificar as informações de expiração de senhas de usuários no sistema Linux. Com ele, é possível definir quando uma senha deve ser alterada, além de configurar períodos de aviso e inatividade.

## Usage
A sintaxe básica do comando `chage` é a seguinte:

```bash
chage [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do comando `chage`:

- `-l, --list`: Lista as informações de expiração da senha do usuário.
- `-m, --mindays MIN`: Define o número mínimo de dias entre as mudanças de senha.
- `-M, --maxdays MAX`: Define o número máximo de dias que a senha é válida.
- `-I, --inactive INACTIVE`: Define o número de dias após a expiração da senha até que a conta seja desativada.
- `-E, --expiredate EXPIRE`: Define a data de expiração da conta.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `chage`:

1. **Listar informações de expiração da senha de um usuário:**

```bash
chage -l nome_do_usuario
```

2. **Definir um mínimo de 7 dias entre mudanças de senha:**

```bash
chage -m 7 nome_do_usuario
```

3. **Definir um máximo de 90 dias para a validade da senha:**

```bash
chage -M 90 nome_do_usuario
```

4. **Definir 30 dias de inatividade após a expiração da senha:**

```bash
chage -I 30 nome_do_usuario
```

5. **Definir uma data de expiração específica para a conta:**

```bash
chage -E 2024-12-31 nome_do_usuario
```

## Tips
- Sempre verifique as configurações atuais de expiração da senha usando `chage -l` antes de fazer alterações.
- Utilize opções de aviso para notificar os usuários antes que suas senhas expirem, garantindo que eles tenham tempo suficiente para realizar a troca.
- Considere a política de segurança da sua organização ao definir os períodos de expiração e inatividade das senhas.