# [Linux] Bash md5sum Uso: Calcular e verificar somas de verificação MD5

## Overview
O comando `md5sum` é utilizado para calcular e verificar a soma de verificação MD5 de arquivos. Essa soma de verificação é uma representação única do conteúdo do arquivo, permitindo verificar a integridade dos dados.

## Usage
A sintaxe básica do comando `md5sum` é a seguinte:

```bash
md5sum [opções] [argumentos]
```

## Common Options
- `-b`: Processa arquivos binários.
- `-c`: Verifica as somas de verificação a partir de um arquivo.
- `-t`: Calcula a soma de verificação apenas para arquivos de texto.
- `--help`: Exibe a ajuda do comando.

## Common Examples

1. **Calcular a soma de verificação de um arquivo:**

```bash
md5sum arquivo.txt
```

2. **Calcular a soma de verificação de vários arquivos:**

```bash
md5sum arquivo1.txt arquivo2.txt
```

3. **Salvar a soma de verificação em um arquivo:**

```bash
md5sum arquivo.txt > arquivo.md5
```

4. **Verificar a soma de verificação a partir de um arquivo:**

```bash
md5sum -c arquivo.md5
```

5. **Calcular a soma de verificação de um arquivo binário:**

```bash
md5sum -b arquivo.bin
```

## Tips
- Sempre verifique a soma de verificação após transferir arquivos importantes para garantir que não houve corrupção.
- Utilize o redirecionamento para salvar somas de verificação em um arquivo, facilitando a verificação futura.
- Combine o `md5sum` com outros comandos, como `find`, para calcular somas de verificação em múltiplos arquivos de forma eficiente.