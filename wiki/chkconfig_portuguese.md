# [Linux] Bash chkconfig Uso: Gerenciar serviços de inicialização

## Overview
O comando `chkconfig` é utilizado em sistemas Linux para gerenciar os serviços que são iniciados automaticamente durante o processo de inicialização do sistema. Ele permite que os administradores ativem ou desativem serviços em diferentes níveis de execução.

## Usage
A sintaxe básica do comando `chkconfig` é a seguinte:

```bash
chkconfig [opções] [serviço] [on|off|reset]
```

## Common Options
- `--list`: Lista todos os serviços e seus estados em diferentes níveis de execução.
- `--add`: Adiciona um novo serviço ao sistema de gerenciamento de inicialização.
- `--del`: Remove um serviço do gerenciamento de inicialização.
- `--level`: Especifica os níveis de execução para os quais o comando deve ser aplicado.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `chkconfig`:

### Listar todos os serviços
```bash
chkconfig --list
```

### Ativar um serviço em todos os níveis de execução
```bash
chkconfig nome_do_serviço on
```

### Desativar um serviço em todos os níveis de execução
```bash
chkconfig nome_do_serviço off
```

### Adicionar um novo serviço
```bash
chkconfig --add nome_do_serviço
```

### Remover um serviço
```bash
chkconfig --del nome_do_serviço
```

### Ativar um serviço apenas em níveis específicos
```bash
chkconfig --level 234 nome_do_serviço on
```

## Tips
- Sempre verifique o estado dos serviços após fazer alterações usando `chkconfig --list`.
- Use o comando com privilégios de superusuário (root) para garantir que você tenha permissão para modificar os serviços.
- Considere usar `systemctl` em distribuições mais recentes que utilizam systemd, pois o `chkconfig` pode não estar disponível.