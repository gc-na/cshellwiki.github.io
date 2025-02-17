# [Linux] Bash tail Uso: Exibir as últimas linhas de um arquivo

## Overview
O comando `tail` é utilizado para exibir as últimas linhas de um arquivo de texto. É especialmente útil para monitorar logs em tempo real ou para visualizar rapidamente o final de arquivos grandes.

## Usage
A sintaxe básica do comando `tail` é a seguinte:

```bash
tail [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `tail`:

- `-n [número]`: Exibe as últimas `número` linhas do arquivo.
- `-f`: Segue o arquivo em tempo real, exibindo novas linhas à medida que são adicionadas.
- `-c [número]`: Exibe os últimos `número` bytes do arquivo.
- `-q`: Não exibe cabeçalhos de arquivos quando múltiplos arquivos são especificados.

## Common Examples

### Exibir as últimas 10 linhas de um arquivo
```bash
tail arquivo.txt
```

### Exibir as últimas 20 linhas de um arquivo
```bash
tail -n 20 arquivo.txt
```

### Seguir um arquivo de log em tempo real
```bash
tail -f /var/log/syslog
```

### Exibir os últimos 100 bytes de um arquivo
```bash
tail -c 100 arquivo.txt
```

### Exibir várias arquivos ao mesmo tempo
```bash
tail -q arquivo1.txt arquivo2.txt
```

## Tips
- Use a opção `-f` para monitorar logs em tempo real, como arquivos de log de servidores, para facilitar a depuração.
- Combine `tail` com outros comandos, como `grep`, para filtrar as linhas exibidas. Por exemplo:
  ```bash
  tail -f arquivo.log | grep "erro"
  ```
- Lembre-se de que o `tail` pode ser usado em arquivos que estão sendo escritos, permitindo que você veja as atualizações à medida que ocorrem.