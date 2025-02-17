# [Linux] Bash hostnamectl Uso: Gerenciar informações do sistema

## Overview
O comando `hostnamectl` é utilizado para consultar e alterar o nome do host e outras configurações relacionadas ao sistema em sistemas operacionais baseados em Linux. Ele faz parte do systemd e fornece uma interface simples para gerenciar informações do sistema.

## Usage
A sintaxe básica do comando `hostnamectl` é a seguinte:

```bash
hostnamectl [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `hostnamectl`:

- `set-hostname`: Define um novo nome de host.
- `set-icon-name`: Define um nome de ícone para o sistema.
- `set-chassis`: Define o tipo de chassi do sistema (por exemplo, desktop, laptop).
- `status`: Exibe informações detalhadas sobre o sistema, incluindo o nome do host atual.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `hostnamectl`:

1. **Exibir informações do sistema:**

   ```bash
   hostnamectl status
   ```

2. **Definir um novo nome de host:**

   ```bash
   sudo hostnamectl set-hostname novo-nome
   ```

3. **Definir o tipo de chassi do sistema:**

   ```bash
   sudo hostnamectl set-chassis laptop
   ```

4. **Definir um nome de ícone:**

   ```bash
   sudo hostnamectl set-icon-name computador
   ```

## Tips
- Sempre use `sudo` ao alterar o nome do host ou outras configurações do sistema, pois essas ações geralmente requerem privilégios de administrador.
- Após alterar o nome do host, pode ser necessário reiniciar o sistema ou desconectar e reconectar para que as alterações tenham efeito completo.
- Utilize o comando `hostname` para verificar rapidamente o nome do host atual sem opções adicionais.