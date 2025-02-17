# [Linux] Bash lvextend Uso: Aumentar o tamanho de volumes lógicos

## Overview
O comando `lvextend` é utilizado para aumentar o tamanho de volumes lógicos em sistemas que utilizam o Logical Volume Manager (LVM). Ele permite que você expanda um volume lógico existente, aumentando sua capacidade de armazenamento sem a necessidade de formatar ou perder dados.

## Usage
A sintaxe básica do comando `lvextend` é a seguinte:

```bash
lvextend [opções] [tamanho] [volume]
```

## Common Options
- `-L, --size`: Define o novo tamanho do volume lógico.
- `-l, --extents`: Especifica o número de extensões a serem adicionadas ao volume lógico.
- `-r, --resizefs`: Redimensiona o sistema de arquivos automaticamente após aumentar o volume.
- `-n, --name`: Altera o nome do volume lógico.

## Common Examples
Aqui estão alguns exemplos práticos de como usar o `lvextend`:

1. **Aumentar o volume lógico para 20 GB:**
   ```bash
   lvextend -L 20G /dev/vg01/lv01
   ```

2. **Adicionar 5 extensões ao volume lógico:**
   ```bash
   lvextend -l +5 /dev/vg01/lv01
   ```

3. **Aumentar o volume lógico e redimensionar o sistema de arquivos automaticamente:**
   ```bash
   lvextend -r -L +10G /dev/vg01/lv01
   ```

4. **Aumentar o volume lógico para 50% do espaço disponível:**
   ```bash
   lvextend -l +50%FREE /dev/vg01/lv01
   ```

## Tips
- Sempre faça um backup dos dados importantes antes de realizar operações de redimensionamento.
- Utilize a opção `-r` para redimensionar o sistema de arquivos automaticamente, economizando tempo e evitando erros.
- Verifique o espaço disponível no grupo de volumes antes de aumentar um volume lógico, usando o comando `vgs`.