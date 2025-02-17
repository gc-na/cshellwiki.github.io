# [Linux] Bash logout uso: Sair da sessão do shell

## Overview
O comando `logout` é utilizado para encerrar uma sessão de shell em sistemas Unix e Linux. Ele é especialmente útil quando você está trabalhando em um terminal e deseja sair da sessão atual, seja ela uma sessão de login ou um subshell.

## Usage
A sintaxe básica do comando é a seguinte:

```bash
logout [options]
```

## Common Options
O comando `logout` não possui muitas opções, mas aqui estão algumas que podem ser relevantes:

- `--help`: Exibe uma mensagem de ajuda com informações sobre o comando.
- `--version`: Mostra a versão do comando `logout`.

## Common Examples

### Exemplo 1: Sair da sessão atual
Para encerrar a sessão do shell atual, você pode simplesmente digitar:

```bash
logout
```

### Exemplo 2: Sair de um subshell
Se você estiver em um subshell (por exemplo, após usar o comando `bash`), você pode sair digitando:

```bash
logout
```

### Exemplo 3: Usando logout em um script
Você pode usar o comando `logout` em um script para encerrar a sessão após a execução de certas tarefas:

```bash
#!/bin/bash
echo "Executando tarefas..."
# Comandos adicionais aqui
logout
```

## Tips
- Sempre salve seu trabalho antes de usar o comando `logout`, pois ele encerrará a sessão imediatamente.
- Se você estiver em um ambiente gráfico, considere usar a opção de sair do sistema através da interface, pois isso pode preservar seu trabalho em andamento.
- O comando `logout` é mais comum em shells de login; em shells não-login, você pode usar `exit` para sair.