# [Linux] Bash last uso: Exibir registros de logins de usuários

## Overview
O comando `last` é utilizado para exibir uma lista dos últimos logins dos usuários no sistema. Ele lê o arquivo de log `/var/log/wtmp`, que armazena informações sobre as sessões de login e logout, permitindo que você veja quem acessou o sistema e quando.

## Usage
A sintaxe básica do comando `last` é a seguinte:

```bash
last [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que você pode usar com o comando `last`:

- `-a`: Mostra o nome do host (hostname) ao lado do nome do usuário.
- `-n [número]`: Limita a saída aos últimos `número` de logins.
- `-x`: Exibe informações sobre as sessões encerradas, além dos logins.
- `-R`: Não exibe o nome do host.

## Common Examples

### Exibir todos os logins
Para ver todos os logins registrados, você pode simplesmente usar:

```bash
last
```

### Limitar a saída
Para mostrar apenas os 5 últimos logins, use:

```bash
last -n 5
```

### Mostrar logins com nome do host
Para incluir o nome do host na saída, utilize:

```bash
last -a
```

### Exibir sessões encerradas
Para ver também as sessões que foram encerradas, execute:

```bash
last -x
```

### Filtrar por um usuário específico
Se você quiser ver os logins de um usuário específico, como `joao`, use:

```bash
last joao
```

## Tips
- Utilize `last -n 10` para rapidamente verificar os últimos 10 logins, o que pode ser útil para auditorias rápidas.
- Combine opções, como `last -a -n 5`, para personalizar a saída conforme suas necessidades.
- Lembre-se de que o arquivo de log pode ser rotacionado, o que significa que os dados mais antigos podem não estar disponíveis se o sistema estiver configurado para manter logs por um período limitado.