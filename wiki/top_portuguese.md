# [Linux] Bash top uso: Monitora processos em tempo real

## Overview
O comando `top` é uma ferramenta poderosa no Linux que permite monitorar os processos em execução em tempo real. Ele fornece uma visão detalhada do uso da CPU, memória e outros recursos do sistema, ajudando os administradores a identificar processos que consomem muitos recursos.

## Usage
A sintaxe básica do comando `top` é a seguinte:

```bash
top [opções]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `top`:

- `-d <segundos>`: Define o intervalo de atualização em segundos.
- `-p <PID>`: Monitora apenas o processo com o ID especificado.
- `-u <usuário>`: Exibe apenas os processos pertencentes ao usuário especificado.
- `-n <número>`: Executa o `top` por um número específico de iterações e depois sai.

## Common Examples

1. **Executar o top com atualização a cada 2 segundos:**
   ```bash
   top -d 2
   ```

2. **Monitorar um processo específico pelo seu PID (por exemplo, 1234):**
   ```bash
   top -p 1234
   ```

3. **Exibir apenas os processos de um usuário específico (por exemplo, "joao"):**
   ```bash
   top -u joao
   ```

4. **Executar o top por 5 iterações e sair:**
   ```bash
   top -n 5
   ```

## Tips
- Utilize a tecla `h` enquanto o `top` está em execução para acessar a ajuda e descobrir mais sobre os comandos interativos disponíveis.
- Para ordenar os processos por uso de CPU, pressione `Shift + P`. Para ordenar por uso de memória, pressione `Shift + M`.
- Para sair do `top`, basta pressionar a tecla `q`.