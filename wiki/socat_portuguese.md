# [Linux] Bash socat Uso: Ferramenta de redirecionamento de fluxo de dados

## Overview
O comando `socat` (SOcket CAT) é uma ferramenta poderosa que permite a criação de conexões entre diferentes fluxos de dados. Ele pode redirecionar dados entre sockets, arquivos, pipes, e muito mais, facilitando a comunicação entre processos e a manipulação de dados em tempo real.

## Usage
A sintaxe básica do comando `socat` é a seguinte:

```bash
socat [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que você pode usar com o `socat`:

- `-u`: Modo não bloqueante (unidirecional).
- `-v`: Modo verbose, que exibe informações detalhadas sobre a operação.
- `TCP:<host>:<port>`: Conecta a um host e porta específicos usando o protocolo TCP.
- `UDP:<host>:<port>`: Conecta a um host e porta específicos usando o protocolo UDP.
- `FILE:<file>`: Lê ou escreve em um arquivo.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `socat`:

1. **Conectar a um servidor TCP:**
   ```bash
   socat - TCP:example.com:80
   ```
   Este comando conecta ao servidor `example.com` na porta 80 usando TCP.

2. **Criar um servidor TCP simples:**
   ```bash
   socat TCP-LISTEN:1234,fork EXEC:/bin/cat
   ```
   Este comando cria um servidor que escuta na porta 1234 e executa o comando `cat` para cada conexão.

3. **Redirecionar um arquivo para um socket:**
   ```bash
   socat FILE:/path/to/file TCP:localhost:1234
   ```
   Este comando lê de um arquivo e envia os dados para um socket TCP em `localhost` na porta 1234.

4. **Conectar dois sockets UDP:**
   ```bash
   socat UDP-LISTEN:1234,fork UDP:localhost:5678
   ```
   Este comando escuta na porta 1234 e redireciona os dados para a porta 5678.

## Tips
- Sempre teste suas conexões em um ambiente seguro antes de usá-las em produção.
- Use a opção `-v` para depuração, especialmente ao solucionar problemas de conexão.
- Combine `socat` com outras ferramentas como `grep` ou `awk` para manipulação avançada de dados.