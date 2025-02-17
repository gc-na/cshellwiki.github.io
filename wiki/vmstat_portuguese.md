# [Linux] Bash vmstat Uso: Monitora estatísticas de sistema

## Overview
O comando `vmstat` (virtual memory statistics) é uma ferramenta útil para monitorar o desempenho do sistema, fornecendo informações sobre processos, memória, troca, I/O e CPU. Ele ajuda os administradores a entender como os recursos do sistema estão sendo utilizados.

## Usage
A sintaxe básica do comando `vmstat` é a seguinte:

```bash
vmstat [opções] [intervalo] [contagem]
```

## Common Options
Aqui estão algumas opções comuns do `vmstat`:

- `-a`: Exibe informações sobre a memória ativa e inativa.
- `-m`: Mostra estatísticas sobre a memória do cache.
- `-s`: Exibe um resumo das estatísticas de memória.
- `-d`: Mostra informações sobre dispositivos de bloco.
- `intervalo`: O tempo em segundos entre as atualizações das estatísticas.
- `contagem`: O número de vezes que as estatísticas devem ser exibidas.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `vmstat`:

1. **Exibir estatísticas padrão**:
   ```bash
   vmstat
   ```

2. **Atualizar a cada 2 segundos, 5 vezes**:
   ```bash
   vmstat 2 5
   ```

3. **Mostrar informações sobre a memória ativa e inativa**:
   ```bash
   vmstat -a
   ```

4. **Exibir um resumo das estatísticas de memória**:
   ```bash
   vmstat -s
   ```

5. **Mostrar estatísticas de dispositivos de bloco**:
   ```bash
   vmstat -d
   ```

## Tips
- Utilize `vmstat` em conjunto com outras ferramentas como `top` e `iostat` para obter uma visão mais completa do desempenho do sistema.
- Monitore o sistema em intervalos regulares durante períodos de carga elevada para identificar gargalos.
- Salve a saída do `vmstat` em um arquivo para análise posterior usando a redireção:
  ```bash
  vmstat 2 5 > vmstat_output.txt
  ```