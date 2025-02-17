# [Linux] Bash rsync Uso: Sincronização de arquivos e diretórios

O comando `rsync` é utilizado para sincronizar arquivos e diretórios entre diferentes locais, seja no mesmo sistema ou em sistemas remotos.

## Overview
O `rsync` é uma ferramenta poderosa que permite transferir e sincronizar arquivos de forma eficiente. Ele utiliza um algoritmo que minimiza a quantidade de dados copiados, transferindo apenas as partes que mudaram.

## Usage
A sintaxe básica do comando `rsync` é a seguinte:

```bash
rsync [opções] [origem] [destino]
```

## Common Options
Aqui estão algumas opções comuns do `rsync`:

- `-a`: Modo de arquivamento; preserva permissões, timestamps, links simbólicos, etc.
- `-v`: Modo verbose; fornece informações detalhadas sobre o que está sendo transferido.
- `-z`: Comprime os dados durante a transferência, útil para conexões lentas.
- `-r`: Sincroniza diretórios recursivamente.
- `--delete`: Remove arquivos no destino que não estão mais na origem.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `rsync`:

1. Sincronizar um diretório local para outro diretório local:

   ```bash
   rsync -av /caminho/origem/ /caminho/destino/
   ```

2. Sincronizar um diretório local para um servidor remoto:

   ```bash
   rsync -av /caminho/origem/ usuario@servidor:/caminho/destino/
   ```

3. Sincronizar um diretório remoto para um diretório local:

   ```bash
   rsync -av usuario@servidor:/caminho/origem/ /caminho/destino/
   ```

4. Sincronizar e excluir arquivos no destino que não existem mais na origem:

   ```bash
   rsync -av --delete /caminho/origem/ /caminho/destino/
   ```

## Tips
- Sempre use a opção `-n` (dry run) para simular a transferência antes de executá-la, garantindo que você não perderá dados acidentalmente.
- Considere usar `-z` para transferências pela internet, pois isso pode acelerar o processo.
- Mantenha backups regulares, especialmente ao usar a opção `--delete`, para evitar perda de dados.