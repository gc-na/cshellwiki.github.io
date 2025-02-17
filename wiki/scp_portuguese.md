# [Linux] Bash scp Uso: Transferência segura de arquivos entre sistemas

## Overview
O comando `scp` (Secure Copy Protocol) é utilizado para transferir arquivos de forma segura entre sistemas, utilizando o protocolo SSH. Ele permite que você copie arquivos ou diretórios de um computador para outro, garantindo a segurança dos dados durante a transferência.

## Usage
A sintaxe básica do comando `scp` é a seguinte:

```bash
scp [opções] [origem] [destino]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o `scp`:

- `-r`: Copia diretórios recursivamente.
- `-P`: Especifica a porta do servidor SSH (note que é uma letra maiúscula).
- `-i`: Especifica um arquivo de chave privada para autenticação.
- `-v`: Ativa o modo verbose, exibindo informações detalhadas sobre a transferência.

## Common Examples

### Copiar um arquivo local para um servidor remoto
```bash
scp arquivo.txt usuario@servidor:/caminho/destino/
```

### Copiar um arquivo de um servidor remoto para o local
```bash
scp usuario@servidor:/caminho/origem/arquivo.txt /caminho/local/
```

### Copiar um diretório inteiro para um servidor remoto
```bash
scp -r /caminho/diretorio usuario@servidor:/caminho/destino/
```

### Copiar um arquivo usando uma porta SSH diferente
```bash
scp -P 2222 arquivo.txt usuario@servidor:/caminho/destino/
```

### Copiar um arquivo usando uma chave privada
```bash
scp -i /caminho/da/chave_privada arquivo.txt usuario@servidor:/caminho/destino/
```

## Tips
- Sempre verifique as permissões do arquivo e do diretório de destino para evitar erros de acesso.
- Utilize a opção `-v` para depuração se você encontrar problemas durante a transferência.
- Para transferências grandes, considere usar `rsync` como uma alternativa, pois ele pode ser mais eficiente em algumas situações.