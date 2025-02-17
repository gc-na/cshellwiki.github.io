# [Linux] Bash split uso: Divide arquivos em partes menores

## Overview
O comando `split` é utilizado no Bash para dividir arquivos grandes em partes menores. Essa funcionalidade é útil quando se deseja manipular ou transferir arquivos que são muito grandes para serem tratados de uma só vez.

## Usage
A sintaxe básica do comando `split` é a seguinte:

```bash
split [opções] [arquivo] [prefixo]
```

## Common Options
Aqui estão algumas opções comuns do comando `split`:

- `-b, --bytes=N`: Divide o arquivo em partes de N bytes.
- `-l, --lines=N`: Divide o arquivo em partes com N linhas.
- `-d, --numeric-suffixes`: Usa sufixos numéricos em vez de letras para nomear os arquivos resultantes.
- `-a, --suffix-length=N`: Especifica o comprimento do sufixo dos arquivos de saída.

## Common Examples

### Dividir um arquivo em partes de 100 linhas
```bash
split -l 100 arquivo.txt parte_
```
Esse comando divide `arquivo.txt` em arquivos menores com 100 linhas cada, nomeando-os com o prefixo `parte_`.

### Dividir um arquivo em partes de 1MB
```bash
split -b 1M arquivo_grande.txt parte_
```
Aqui, `arquivo_grande.txt` é dividido em partes de 1 megabyte.

### Usar sufixos numéricos
```bash
split -d -l 50 arquivo.txt parte_
```
Esse comando divide `arquivo.txt` em partes de 50 linhas, utilizando sufixos numéricos para os arquivos resultantes.

### Especificar o comprimento do sufixo
```bash
split -a 3 -b 500k arquivo.txt parte_
```
Neste exemplo, o arquivo é dividido em partes de 500 kilobytes, e os arquivos resultantes terão sufixos de 3 dígitos.

## Tips
- Sempre verifique o tamanho das partes resultantes para garantir que elas atendem às suas necessidades.
- Use o comando `cat` para juntar as partes novamente, se necessário, por exemplo: `cat parte_* > arquivo_reconstruido.txt`.
- Considere usar o comando `gzip` em conjunto com `split` para compactar arquivos grandes antes de dividi-los, economizando espaço em disco.