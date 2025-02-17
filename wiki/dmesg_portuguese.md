# [Linux] Bash dmesg Uso: Exibir mensagens do kernel

## Overview
O comando `dmesg` é utilizado para exibir mensagens do buffer do anel do kernel do Linux. Essas mensagens geralmente incluem informações sobre o hardware, drivers e eventos do sistema, sendo útil para diagnosticar problemas e monitorar o desempenho do sistema.

## Usage
A sintaxe básica do comando `dmesg` é a seguinte:

```bash
dmesg [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `dmesg`:

- `-C`: Limpa o buffer de mensagens do kernel.
- `-c`: Limpa o buffer de mensagens e exibe as mensagens atuais.
- `-n <nível>`: Define o nível de log para mensagens que devem ser exibidas.
- `-T`: Exibe as mensagens com timestamps legíveis por humanos.
- `--follow`: Monitora continuamente novas mensagens do kernel.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `dmesg`:

1. **Exibir todas as mensagens do kernel:**
   ```bash
   dmesg
   ```

2. **Exibir mensagens com timestamps legíveis:**
   ```bash
   dmesg -T
   ```

3. **Limpar o buffer de mensagens e exibir as atuais:**
   ```bash
   dmesg -c
   ```

4. **Monitorar novas mensagens do kernel em tempo real:**
   ```bash
   dmesg --follow
   ```

5. **Definir o nível de log para exibir apenas mensagens de erro:**
   ```bash
   dmesg -n 1
   ```

## Tips
- Utilize `dmesg -T` para facilitar a leitura das mensagens, especialmente ao depurar problemas.
- Combine `dmesg` com `grep` para filtrar mensagens específicas, como por exemplo: 
  ```bash
  dmesg | grep error
  ```
- Verifique regularmente as mensagens do kernel após a instalação de novos drivers ou hardware para garantir que tudo esteja funcionando corretamente.