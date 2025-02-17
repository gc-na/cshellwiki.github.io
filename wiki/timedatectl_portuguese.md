# [Linux] Bash timedatectl Uso: Gerenciar data e hora do sistema

## Overview
O comando `timedatectl` é uma ferramenta utilizada para consultar e alterar a configuração de data e hora do sistema em sistemas operacionais baseados em Linux. Ele também permite gerenciar informações de fuso horário e sincronização de tempo.

## Usage
A sintaxe básica do comando `timedatectl` é a seguinte:

```bash
timedatectl [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o `timedatectl`:

- `status`: Mostra o status atual da data, hora e fuso horário.
- `set-time`: Define a data e hora do sistema.
- `set-timezone`: Altera o fuso horário do sistema.
- `set-ntp`: Habilita ou desabilita a sincronização automática de tempo via NTP (Network Time Protocol).
- `list-timezones`: Lista todos os fusos horários disponíveis.

## Common Examples

### Verificar o status atual
Para verificar a data, hora e fuso horário atuais do sistema, use:

```bash
timedatectl status
```

### Definir a data e hora
Para definir a data e hora do sistema, utilize o seguinte comando, substituindo `YYYY-MM-DD HH:MM:SS` pela data e hora desejadas:

```bash
timedatectl set-time '2023-10-01 12:30:00'
```

### Alterar o fuso horário
Para alterar o fuso horário, primeiro você pode listar os fusos horários disponíveis e, em seguida, definir o desejado. Por exemplo, para definir o fuso horário para "America/Sao_Paulo":

```bash
timedatectl set-timezone America/Sao_Paulo
```

### Habilitar a sincronização NTP
Para habilitar a sincronização automática de tempo via NTP, execute:

```bash
timedatectl set-ntp true
```

### Listar fusos horários
Para listar todos os fusos horários disponíveis, use:

```bash
timedatectl list-timezones
```

## Tips
- Sempre verifique o status atual após fazer alterações para garantir que as configurações foram aplicadas corretamente.
- Utilize a opção `list-timezones` para encontrar o fuso horário correto antes de alterá-lo.
- Considere habilitar a sincronização NTP para manter a hora do sistema precisa, especialmente em servidores.