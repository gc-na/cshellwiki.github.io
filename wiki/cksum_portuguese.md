# [Linux] Bash cksum: Calcula e exibe o checksum de arquivos

## Overview
O comando `cksum` é utilizado para calcular e exibir o valor de checksum (soma de verificação) de um arquivo. Ele fornece um valor numérico que pode ser usado para verificar a integridade dos dados, ajudando a identificar alterações ou corrupções em arquivos.

## Usage
A sintaxe básica do comando `cksum` é a seguinte:

```bash
cksum [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `cksum`:

- `-a, --algorithm=ALGO`: Especifica o algoritmo de checksum a ser usado.
- `--help`: Exibe uma mensagem de ajuda com informações sobre o uso do comando.
- `--version`: Mostra a versão do comando `cksum`.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `cksum`:

1. Calcular o checksum de um arquivo:
   ```bash
   cksum arquivo.txt
   ```

2. Calcular o checksum de vários arquivos:
   ```bash
   cksum arquivo1.txt arquivo2.txt
   ```

3. Usar o `cksum` com um redirecionamento para salvar a saída em um arquivo:
   ```bash
   cksum arquivo.txt > checksum.txt
   ```

4. Exibir a ajuda do comando:
   ```bash
   cksum --help
   ```

## Tips
- Sempre verifique o checksum de arquivos importantes após transferências ou cópias para garantir que não houve corrupção.
- Combine o `cksum` com outros comandos, como `find`, para verificar múltiplos arquivos em diretórios.
- Utilize o redirecionamento para salvar os checksums em um arquivo para referência futura.