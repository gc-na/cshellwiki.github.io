# [Linux] Bash watch uso: Atualiza a saída de um comando periodicamente

## Overview
O comando `watch` é utilizado para executar periodicamente um comando e exibir sua saída em tempo real no terminal. Isso é útil para monitorar mudanças em arquivos, processos ou qualquer outra saída de comando que você deseje observar ao longo do tempo.

## Usage
A sintaxe básica do comando `watch` é a seguinte:

```bash
watch [opções] [comando]
```

## Common Options
Aqui estão algumas opções comuns que você pode usar com o comando `watch`:

- `-n, --interval <segundos>`: Define o intervalo em segundos entre as execuções do comando. O padrão é 2 segundos.
- `-d, --differences`: Destaca as diferenças entre as saídas sucessivas do comando.
- `-t, --no-title`: Remove a linha de título que exibe o comando e o intervalo.
- `-x, --exec`: Permite executar um comando com argumentos.

## Common Examples

### Exemplo 1: Monitorar o uso de memória
Para monitorar o uso de memória do sistema a cada 5 segundos, você pode usar:

```bash
watch -n 5 free -h
```

### Exemplo 2: Verificar processos em execução
Para observar os processos em execução e suas informações a cada 2 segundos, utilize:

```bash
watch ps aux
```

### Exemplo 3: Destacar mudanças em um arquivo
Para monitorar um diretório e destacar as mudanças em um arquivo específico, você pode fazer:

```bash
watch -d ls -l /caminho/do/diretorio
```

### Exemplo 4: Monitorar espaço em disco
Para verificar o espaço em disco disponível a cada 10 segundos, execute:

```bash
watch -n 10 df -h
```

## Tips
- Use a opção `-d` para facilitar a visualização de mudanças importantes nas saídas.
- Ajuste o intervalo com `-n` para um tempo que faça sentido para o que você está monitorando, evitando atualizações muito frequentes que podem sobrecarregar o terminal.
- Combine `watch` com outros comandos para monitorar logs ou saídas de scripts, como `tail -f`, para um acompanhamento mais dinâmico.