# [Linux] Bash journalctl uso: Visualizar logs do sistema

## Overview
O comando `journalctl` é utilizado para visualizar os logs do sistema gerenciados pelo systemd. Ele permite acessar informações detalhadas sobre eventos do sistema, serviços e aplicativos, facilitando a análise e a solução de problemas.

## Usage
A sintaxe básica do comando `journalctl` é a seguinte:

```bash
journalctl [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o `journalctl`:

- `-b`: Exibe logs da sessão atual do boot.
- `-f`: Segue os logs em tempo real, semelhante ao comando `tail -f`.
- `--since "data"`: Filtra os logs a partir de uma data específica.
- `--until "data"`: Filtra os logs até uma data específica.
- `-u <serviço>`: Mostra apenas os logs de um serviço específico.
- `-p <prioridade>`: Filtra logs por prioridade (ex: `err`, `warning`, `info`).

## Common Examples
Aqui estão alguns exemplos práticos do uso do `journalctl`:

1. **Exibir todos os logs**:
   ```bash
   journalctl
   ```

2. **Exibir logs da sessão atual do boot**:
   ```bash
   journalctl -b
   ```

3. **Seguir os logs em tempo real**:
   ```bash
   journalctl -f
   ```

4. **Filtrar logs a partir de uma data específica**:
   ```bash
   journalctl --since "2023-10-01"
   ```

5. **Filtrar logs até uma data específica**:
   ```bash
   journalctl --until "2023-10-10"
   ```

6. **Mostrar logs de um serviço específico**:
   ```bash
   journalctl -u nginx.service
   ```

7. **Filtrar logs por prioridade**:
   ```bash
   journalctl -p err
   ```

## Tips
- Utilize `journalctl -b -1` para visualizar os logs do boot anterior.
- Combine opções, como `journalctl -u nginx.service -f`, para monitorar logs de um serviço específico em tempo real.
- Use `--no-pager` para exibir todos os logs de uma vez, sem paginar a saída.
- Para exportar logs para um arquivo, você pode redirecionar a saída: `journalctl > logs.txt`.