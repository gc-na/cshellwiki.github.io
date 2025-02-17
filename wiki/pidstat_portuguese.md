# [Linux] Bash pidstat Uso: Monitora estatísticas de desempenho de processos

## Overview
O comando `pidstat` é uma ferramenta do pacote `sysstat` que permite monitorar o desempenho de processos em tempo real. Ele fornece informações detalhadas sobre o uso de CPU, memória e outras métricas de desempenho para processos específicos em execução no sistema.

## Usage
A sintaxe básica do comando `pidstat` é a seguinte:

```bash
pidstat [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `pidstat`:

- `-h`: Mostra a saída em formato legível, omitindo os cabeçalhos de coluna.
- `-r`: Exibe informações sobre o uso de memória.
- `-u`: Mostra estatísticas de uso da CPU.
- `-p <PID>`: Especifica o ID do processo a ser monitorado.
- `-t`: Exibe informações sobre threads individuais de um processo.

## Common Examples
Aqui estão alguns exemplos práticos de uso do `pidstat`:

1. **Monitorar o uso da CPU de todos os processos:**
   ```bash
   pidstat -u 1
   ```
   Este comando exibe o uso da CPU de todos os processos a cada segundo.

2. **Monitorar um processo específico pelo PID:**
   ```bash
   pidstat -p 1234 1
   ```
   Substitua `1234` pelo ID do processo que você deseja monitorar. O comando mostrará as estatísticas a cada segundo.

3. **Exibir informações sobre o uso de memória:**
   ```bash
   pidstat -r 1
   ```
   Este comando fornece informações sobre o uso de memória de todos os processos a cada segundo.

4. **Monitorar threads de um processo específico:**
   ```bash
   pidstat -t -p 1234 1
   ```
   Isso mostrará estatísticas detalhadas para cada thread do processo especificado.

## Tips
- Utilize o `pidstat` em combinação com outros comandos como `grep` para filtrar resultados específicos.
- Experimente usar o `-h` para uma saída mais limpa e legível, especialmente quando você está monitorando muitos processos.
- Considere redirecionar a saída para um arquivo para análise posterior, usando `> output.txt`.