# [Linux] Bash ps Uso: Exibir processos em execução

## Overview
O comando `ps` é utilizado para exibir informações sobre os processos em execução no sistema. Ele fornece uma visão instantânea dos processos, permitindo que os usuários monitorem o que está ativo e obtenham detalhes como o uso de CPU e memória.

## Usage
A sintaxe básica do comando `ps` é a seguinte:

```bash
ps [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do comando `ps`:

- `-e` ou `-A`: Exibe todos os processos em execução.
- `-f`: Exibe informações completas sobre os processos, incluindo o comando completo e os parâmetros.
- `-u [usuario]`: Exibe processos pertencentes a um usuário específico.
- `-aux`: Exibe todos os processos com informações detalhadas (uma combinação de opções).
- `--sort`: Permite ordenar a saída com base em um critério específico, como uso de memória ou CPU.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `ps`:

1. **Exibir todos os processos em execução:**
   ```bash
   ps -e
   ```

2. **Exibir processos com detalhes completos:**
   ```bash
   ps -f
   ```

3. **Exibir processos de um usuário específico:**
   ```bash
   ps -u nome_do_usuario
   ```

4. **Exibir todos os processos com informações detalhadas:**
   ```bash
   ps aux
   ```

5. **Ordenar a saída pelo uso de memória:**
   ```bash
   ps aux --sort=-%mem
   ```

## Tips
- Utilize `ps aux | grep [nome_do_processo]` para filtrar processos específicos.
- Combine `ps` com outros comandos, como `less`, para facilitar a leitura de saídas longas: `ps aux | less`.
- Lembre-se de que o `ps` fornece uma captura instantânea; para monitoramento contínuo, considere usar o comando `top`.