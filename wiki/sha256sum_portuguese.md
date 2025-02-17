# [Linux] Bash sha256sum Uso: Calcular e verificar somas de verificação SHA-256

## Overview
O comando `sha256sum` é utilizado para calcular e verificar a soma de verificação SHA-256 de arquivos. Essa soma de verificação é uma representação única do conteúdo do arquivo, sendo útil para garantir a integridade dos dados.

## Usage
A sintaxe básica do comando `sha256sum` é a seguinte:

```bash
sha256sum [opções] [argumentos]
```

## Common Options
- `-b`: Calcula a soma de verificação em modo binário.
- `-c`: Verifica as somas de verificação a partir de um arquivo.
- `--help`: Exibe uma mensagem de ajuda com as opções disponíveis.
- `--version`: Mostra a versão do `sha256sum`.

## Common Examples
Aqui estão alguns exemplos práticos de como usar o `sha256sum`:

### Calcular a soma de verificação de um arquivo
```bash
sha256sum arquivo.txt
```

### Calcular a soma de verificação de vários arquivos
```bash
sha256sum arquivo1.txt arquivo2.txt
```

### Salvar a soma de verificação em um arquivo
```bash
sha256sum arquivo.txt > soma.txt
```

### Verificar a soma de verificação a partir de um arquivo
```bash
sha256sum -c soma.txt
```

### Calcular a soma de verificação em modo binário
```bash
sha256sum -b arquivo.bin
```

## Tips
- Sempre verifique a soma de verificação de arquivos baixados da internet para garantir que não foram corrompidos ou alterados.
- Utilize o redirecionamento para salvar somas de verificação em arquivos para futuras referências.
- Combine o `sha256sum` com outros comandos, como `find`, para calcular somas de verificação de múltiplos arquivos em diretórios.