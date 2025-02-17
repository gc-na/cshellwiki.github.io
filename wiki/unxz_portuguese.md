# [Linux] Bash unxz Uso: Descompactar arquivos .xz

## Overview
O comando `unxz` é utilizado para descompactar arquivos que estão no formato `.xz`, que é um formato de compressão de dados eficiente. Ele é frequentemente usado para reduzir o tamanho de arquivos, facilitando o armazenamento e a transferência.

## Usage
A sintaxe básica do comando `unxz` é a seguinte:

```bash
unxz [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que você pode usar com o `unxz`:

- `-k`, `--keep`: Mantém o arquivo original após a descompactação.
- `-f`, `--force`: Força a descompactação, mesmo que o arquivo de saída já exista.
- `-v`, `--verbose`: Exibe informações detalhadas sobre o processo de descompactação.

## Common Examples
Aqui estão alguns exemplos práticos de como usar o comando `unxz`:

1. **Descompactar um arquivo .xz**:
   ```bash
   unxz arquivo.xz
   ```

2. **Descompactar e manter o arquivo original**:
   ```bash
   unxz -k arquivo.xz
   ```

3. **Forçar a descompactação, sobrescrevendo arquivos existentes**:
   ```bash
   unxz -f arquivo.xz
   ```

4. **Descompactar um arquivo e ver o progresso**:
   ```bash
   unxz -v arquivo.xz
   ```

## Tips
- Sempre verifique se você tem espaço suficiente em disco antes de descompactar arquivos grandes.
- Use a opção `-k` se você quiser manter o arquivo compactado original para referência futura.
- Combine `unxz` com outros comandos, como `tar`, para descompactar arquivos tar.xz diretamente, usando `tar -xvf arquivo.tar.xz`.