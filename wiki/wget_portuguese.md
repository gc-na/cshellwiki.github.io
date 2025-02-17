# [Linux] Bash wget Uso: Ferramenta para download de arquivos da web

## Overview
O comando `wget` é uma ferramenta de linha de comando utilizada para baixar arquivos da web. Ele suporta diversos protocolos, como HTTP, HTTPS e FTP, permitindo que os usuários façam downloads de forma simples e eficiente.

## Usage
A sintaxe básica do comando `wget` é a seguinte:

```bash
wget [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `wget`:

- `-O [arquivo]`: Especifica o nome do arquivo de saída.
- `-q`: Executa o comando em modo silencioso, sem exibir mensagens.
- `-c`: Continua um download interrompido.
- `--limit-rate=[taxa]`: Limita a taxa de download a um valor específico.
- `-r`: Realiza o download recursivo de diretórios.

## Common Examples
Aqui estão alguns exemplos práticos de como usar o `wget`:

1. **Baixar um arquivo simples:**

```bash
wget https://example.com/arquivo.zip
```

2. **Baixar um arquivo e renomeá-lo:**

```bash
wget -O novo_nome.zip https://example.com/arquivo.zip
```

3. **Baixar um arquivo em modo silencioso:**

```bash
wget -q https://example.com/arquivo.zip
```

4. **Continuar um download interrompido:**

```bash
wget -c https://example.com/arquivo.zip
```

5. **Baixar um site inteiro de forma recursiva:**

```bash
wget -r https://example.com
```

## Tips
- Sempre verifique a URL antes de iniciar o download para evitar erros.
- Use a opção `-c` para economizar tempo e largura de banda ao continuar downloads interrompidos.
- Para downloads grandes, considere usar a opção `--limit-rate` para não sobrecarregar sua conexão de internet.