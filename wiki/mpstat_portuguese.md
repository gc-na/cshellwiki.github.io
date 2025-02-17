# [Linux] Bash mpstat Uso: Monitora a utilização da CPU

## Overview
O comando `mpstat` é uma ferramenta de monitoramento que exibe estatísticas de utilização da CPU em sistemas Linux. Ele fornece informações detalhadas sobre a carga da CPU, permitindo que os usuários analisem o desempenho do sistema em tempo real.

## Usage
A sintaxe básica do comando `mpstat` é a seguinte:

```bash
mpstat [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `mpstat`:

- `-P ALL`: Exibe estatísticas para todas as CPUs.
- `-u`: Mostra a utilização da CPU.
- `-r`: Exibe estatísticas de I/O.
- `-h`: Exibe a ajuda com as opções disponíveis.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `mpstat`:

1. **Exibir estatísticas de todas as CPUs**:
   ```bash
   mpstat -P ALL
   ```

2. **Mostrar a utilização da CPU a cada 2 segundos**:
   ```bash
   mpstat 2
   ```

3. **Exibir estatísticas de I/O**:
   ```bash
   mpstat -r
   ```

4. **Exibir a utilização da CPU com um intervalo de 5 segundos**:
   ```bash
   mpstat -u 5
   ```

## Tips
- Utilize a opção `-P ALL` para obter uma visão completa do desempenho de todas as CPUs em sistemas multicore.
- Combine `mpstat` com outras ferramentas como `grep` para filtrar informações específicas.
- Monitore o desempenho da CPU durante períodos de alta carga para identificar gargalos e otimizar o sistema.