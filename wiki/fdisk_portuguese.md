# [Linux] Bash fdisk uso: Gerenciar partições de disco

## Overview
O comando `fdisk` é uma ferramenta de linha de comando utilizada para manipular tabelas de partição em sistemas Linux. Ele permite criar, excluir e modificar partições em discos rígidos, facilitando a gestão do espaço em disco.

## Usage
A sintaxe básica do comando `fdisk` é a seguinte:

```bash
fdisk [opções] [dispositivo]
```

## Common Options
Aqui estão algumas opções comuns do `fdisk` com explicações breves:

- `-l`: Lista todas as partições em todos os dispositivos.
- `-u`: Usa setores como unidade de medida em vez de cilindros.
- `-n`: Cria uma nova partição.
- `-d`: Exclui uma partição existente.
- `-t`: Altera o tipo de uma partição.

## Common Examples

### Listar Partições
Para listar todas as partições em todos os dispositivos, use:

```bash
fdisk -l
```

### Criar uma Nova Partição
Para criar uma nova partição em um dispositivo específico (por exemplo, `/dev/sda`), inicie o `fdisk` e siga as instruções interativas:

```bash
fdisk /dev/sda
```

Dentro do `fdisk`, você pode usar `n` para criar uma nova partição.

### Excluir uma Partição
Para excluir uma partição, inicie o `fdisk` e selecione a partição que deseja remover:

```bash
fdisk /dev/sda
```

Depois, use `d` para deletar a partição.

### Alterar o Tipo de Partição
Para alterar o tipo de uma partição, inicie o `fdisk` e use:

```bash
fdisk /dev/sda
```

Em seguida, use `t` para alterar o tipo e forneça o número da partição e o novo tipo.

## Tips
- Sempre faça backup dos seus dados antes de modificar partições, pois alterações podem resultar em perda de dados.
- Utilize o comando `partprobe` após usar o `fdisk` para notificar o sistema sobre as alterações nas partições.
- Familiarize-se com as opções interativas do `fdisk` para uma experiência mais eficiente ao gerenciar partições.