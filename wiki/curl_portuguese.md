# [Linux] Bash curl Uso: Ferramenta para transferir dados da web

## Overview
O comando `curl` é uma ferramenta de linha de comando utilizada para transferir dados de ou para um servidor, utilizando diversos protocolos como HTTP, HTTPS, FTP, entre outros. É amplamente utilizado para fazer requisições a APIs, baixar arquivos e testar a conectividade de rede.

## Usage
A sintaxe básica do comando `curl` é a seguinte:

```bash
curl [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `curl`:

- `-X`: Especifica o método HTTP a ser utilizado (GET, POST, PUT, DELETE, etc.).
- `-d`: Envia dados no corpo da requisição (usado principalmente com POST).
- `-H`: Adiciona um cabeçalho HTTP à requisição.
- `-o`: Salva a saída em um arquivo em vez de exibi-la no terminal.
- `-I`: Obtém apenas os cabeçalhos da resposta.
- `-L`: Segue redirecionamentos.

## Common Examples

### 1. Fazer uma requisição GET
Para fazer uma requisição GET simples a um URL:

```bash
curl https://api.exemplo.com/dados
```

### 2. Fazer uma requisição POST
Para enviar dados em uma requisição POST:

```bash
curl -X POST -d "nome=João&idade=30" https://api.exemplo.com/usuarios
```

### 3. Adicionar cabeçalhos
Para adicionar um cabeçalho à requisição:

```bash
curl -H "Authorization: Bearer seu_token_aqui" https://api.exemplo.com/protegido
```

### 4. Baixar um arquivo
Para baixar um arquivo e salvá-lo com um nome específico:

```bash
curl -o arquivo.zip https://exemplo.com/arquivo.zip
```

### 5. Obter apenas cabeçalhos
Para obter apenas os cabeçalhos da resposta:

```bash
curl -I https://api.exemplo.com
```

## Tips
- Utilize a opção `-L` se você estiver lidando com URLs que podem redirecionar para outros locais.
- Para testar APIs, combine `curl` com `jq` para formatar a saída JSON de forma legível.
- Sempre verifique a documentação da API que você está utilizando para entender os parâmetros e métodos suportados.