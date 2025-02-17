# [Linux] Bash sha512sum Uso: Gera somas de verificação SHA-512

## Overview
O comando `sha512sum` é utilizado para calcular e verificar somas de verificação SHA-512 de arquivos. Essa função é útil para garantir a integridade dos dados, permitindo que você verifique se um arquivo foi alterado ou corrompido.

## Usage
A sintaxe básica do comando `sha512sum` é a seguinte:

```bash
sha512sum [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o `sha512sum`:

- `-b`: Lê o arquivo em modo binário.
- `-c`: Verifica as somas de verificação a partir de um arquivo.
- `-h`: Exibe uma ajuda com as opções disponíveis.
- `--tag`: Gera uma saída no formato de tag.

## Common Examples
Aqui estão alguns exemplos práticos de como usar o `sha512sum`:

1. **Calcular a soma de verificação de um arquivo:**

```bash
sha512sum arquivo.txt
```

2. **Calcular a soma de verificação de vários arquivos:**

```bash
sha512sum arquivo1.txt arquivo2.txt
```

3. **Salvar a soma de verificação em um arquivo:**

```bash
sha512sum arquivo.txt > arquivo.sha512
```

4. **Verificar somas de verificação a partir de um arquivo:**

```bash
sha512sum -c arquivo.sha512
```

5. **Calcular a soma de verificação de um arquivo em modo binário:**

```bash
sha512sum -b arquivo.bin
```

## Tips
- Sempre verifique as somas de verificação após transferir arquivos importantes para garantir que não houve corrupção.
- Utilize a opção `-c` com um arquivo que contém somas de verificação para verificar múltiplos arquivos de uma só vez.
- Mantenha cópias das somas de verificação em um local seguro, especialmente para arquivos críticos.