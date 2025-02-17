# [Linux] Bash lvcreate Uso: Criação de volumes lógicos

## Overview
O comando `lvcreate` é utilizado para criar volumes lógicos em um sistema de gerenciamento de volumes lógicos (LVM). Ele permite que os usuários aloque espaço em disco de forma flexível, facilitando a gestão de armazenamento em sistemas Linux.

## Usage
A sintaxe básica do comando `lvcreate` é a seguinte:

```bash
lvcreate [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o `lvcreate`:

- `-n, --name <nome>`: Especifica o nome do volume lógico a ser criado.
- `-L, --size <tamanho>`: Define o tamanho do volume lógico. O tamanho pode ser especificado em megabytes (M), gigabytes (G), etc.
- `-l, --extents <número>`: Define o número de extensões a serem alocadas para o volume lógico.
- `-C, --mirrors <número>`: Cria um volume lógico espelhado com o número especificado de cópias.
- `-Z, --zero n`: Define se o volume lógico deve ser inicializado com zeros.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `lvcreate`:

1. Criar um volume lógico chamado `meu_volume` com 10G de tamanho:

   ```bash
   lvcreate -n meu_volume -L 10G vg_exemplo
   ```

2. Criar um volume lógico de 5G usando extensões:

   ```bash
   lvcreate -n volume_extensao -l 5 vg_exemplo
   ```

3. Criar um volume lógico espelhado com 2 cópias:

   ```bash
   lvcreate -n volume_espelhado -L 20G -m 1 vg_exemplo
   ```

4. Criar um volume lógico e inicializá-lo com zeros:

   ```bash
   lvcreate -n volume_zero -L 15G -Z y vg_exemplo
   ```

## Tips
- Sempre verifique o espaço disponível no grupo de volumes antes de criar um novo volume lógico para evitar erros.
- Utilize nomes descritivos para seus volumes lógicos, facilitando a identificação futura.
- Considere o uso de volumes espelhados para aumentar a segurança dos dados, especialmente em ambientes críticos.