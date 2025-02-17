# [Linux] Bash dstat Uso: Monitoramento de recursos do sistema em tempo real

## Overview
O comando `dstat` é uma ferramenta poderosa para monitorar recursos do sistema em tempo real. Ele combina as funcionalidades de várias ferramentas como `vmstat`, `iostat`, `netstat`, entre outras, permitindo que você visualize informações sobre CPU, memória, disco e rede de forma integrada.

## Usage
A sintaxe básica do comando `dstat` é a seguinte:

```bash
dstat [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que você pode usar com o `dstat`:

- `-c`: Mostra a utilização da CPU.
- `-d`: Exibe a atividade do disco.
- `-n`: Mostra a atividade da rede.
- `-m`: Exibe informações sobre a memória.
- `--time`: Adiciona um timestamp à saída.
- `-r`: Mostra a atividade de leitura e escrita no disco.

## Common Examples
Aqui estão alguns exemplos práticos de como usar o `dstat`:

1. **Monitorar CPU e Disco:**
   ```bash
   dstat -cd
   ```

2. **Monitorar Rede e Memória:**
   ```bash
   dstat -nm
   ```

3. **Monitorar todos os recursos com timestamp:**
   ```bash
   dstat --time -cdmn
   ```

4. **Salvar a saída em um arquivo:**
   ```bash
   dstat -cdmn --output estatisticas.csv
   ```

5. **Monitorar a utilização da CPU com intervalos de 2 segundos:**
   ```bash
   dstat -c 2
   ```

## Tips
- Utilize a opção `--output` para registrar a saída em um arquivo, facilitando a análise posterior.
- Combine várias opções para obter uma visão abrangente do desempenho do sistema.
- Experimente diferentes intervalos de tempo para ver como os recursos variam sob diferentes cargas de trabalho.
- Lembre-se de executar o `dstat` com permissões adequadas, especialmente se você estiver monitorando recursos em um sistema restrito.