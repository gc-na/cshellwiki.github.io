# [Linux] Bash iostat Uso: Monitora o desempenho do sistema

## Overview
O comando `iostat` é uma ferramenta utilizada para monitorar o desempenho de entrada e saída (I/O) de dispositivos e partições em sistemas Linux. Ele fornece informações sobre a utilização da CPU e estatísticas de I/O, ajudando na identificação de gargalos de desempenho.

## Usage
A sintaxe básica do comando `iostat` é a seguinte:

```bash
iostat [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `iostat`:

- `-c`: Exibe apenas as estatísticas da CPU.
- `-d`: Mostra as estatísticas de I/O dos dispositivos.
- `-x`: Fornece informações detalhadas sobre os dispositivos.
- `-m`: Exibe os dados em megabytes por segundo.
- `-t`: Adiciona um timestamp às saídas.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `iostat`:

1. **Exibir estatísticas básicas de I/O:**
   ```bash
   iostat
   ```

2. **Mostrar apenas as estatísticas da CPU:**
   ```bash
   iostat -c
   ```

3. **Exibir estatísticas detalhadas de dispositivos:**
   ```bash
   iostat -d -x
   ```

4. **Mostrar estatísticas em megabytes por segundo:**
   ```bash
   iostat -m
   ```

5. **Exibir estatísticas com um intervalo de tempo de 5 segundos:**
   ```bash
   iostat 5
   ```

## Tips
- Utilize a opção `-t` para adicionar timestamps, facilitando a análise de desempenho ao longo do tempo.
- Combine `iostat` com outras ferramentas como `vmstat` e `mpstat` para obter uma visão mais abrangente do desempenho do sistema.
- Monitore regularmente o desempenho do sistema em ambientes de produção para identificar e resolver problemas antes que se tornem críticos.