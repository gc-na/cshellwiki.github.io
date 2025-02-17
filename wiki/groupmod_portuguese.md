# [Linux] Bash groupmod Uso: Modificar grupos de usuários

## Overview
O comando `groupmod` é utilizado para modificar grupos de usuários no sistema Linux. Ele permite que você altere propriedades de um grupo existente, como seu nome ou identificador (GID).

## Usage
A sintaxe básica do comando `groupmod` é a seguinte:

```bash
groupmod [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que você pode usar com o comando `groupmod`:

- `-n, --new-name NOME`: Altera o nome do grupo para o nome especificado.
- `-g, --gid GID`: Altera o identificador do grupo (GID) para o valor especificado.
- `-o, --non-unique`: Permite a criação de um GID que não é único.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `groupmod`:

1. **Alterar o nome de um grupo**:
   Para alterar o nome do grupo de `antigos` para `novos`, você pode usar:
   ```bash
   groupmod -n novos antigos
   ```

2. **Alterar o GID de um grupo**:
   Para mudar o GID do grupo `desenvolvedores` para `2001`, você pode executar:
   ```bash
   groupmod -g 2001 desenvolvedores
   ```

3. **Alterar o nome e o GID de um grupo**:
   Para mudar o nome do grupo `testes` para `experimentos` e o GID para `3000`, use:
   ```bash
   groupmod -n experimentos -g 3000 testes
   ```

## Tips
- Sempre verifique se o novo nome ou GID que você está tentando usar não está em conflito com outros grupos existentes.
- Use o comando `getent group` para listar grupos e verificar as alterações feitas.
- É recomendável fazer backup de arquivos de configuração antes de realizar alterações significativas em grupos de usuários.