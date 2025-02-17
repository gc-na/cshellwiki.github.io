# [Linux] Bash df Uso: Exibir informações sobre o uso do sistema de arquivos

## Overview
O comando `df` (disk free) é utilizado para exibir informações sobre o espaço em disco disponível e utilizado em sistemas de arquivos montados. Ele fornece uma visão geral do uso do disco, permitindo que os usuários monitorem a capacidade de armazenamento.

## Usage
A sintaxe básica do comando `df` é a seguinte:

```bash
df [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do comando `df`:

- `-h`: Exibe os tamanhos em formato legível por humanos (ex.: KB, MB, GB).
- `-T`: Mostra o tipo de sistema de arquivos.
- `-a`: Inclui sistemas de arquivos que têm 0 blocos.
- `-i`: Exibe informações sobre inodes em vez de blocos.

## Common Examples

1. **Exibir informações básicas sobre o uso do disco:**
   ```bash
   df
   ```

2. **Exibir informações em formato legível por humanos:**
   ```bash
   df -h
   ```

3. **Exibir informações incluindo o tipo de sistema de arquivos:**
   ```bash
   df -T
   ```

4. **Exibir informações sobre inodes:**
   ```bash
   df -i
   ```

5. **Exibir informações de todos os sistemas de arquivos, incluindo aqueles com 0 blocos:**
   ```bash
   df -a
   ```

## Tips
- Use a opção `-h` sempre que precisar de uma visualização mais amigável dos dados, especialmente em sistemas com grandes volumes de armazenamento.
- Combine opções para obter informações mais detalhadas. Por exemplo, `df -hT` fornece uma visão clara e informativa sobre o uso do disco e o tipo de sistema de arquivos.
- Verifique regularmente o uso do disco para evitar problemas de espaço, especialmente em servidores e sistemas críticos.