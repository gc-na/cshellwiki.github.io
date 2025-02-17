# [Linux] Bash time uso: Medir o tempo de execução de comandos

## Overview
O comando `time` no Bash é utilizado para medir o tempo que um comando leva para ser executado. Ele fornece informações sobre o tempo real, o tempo de CPU utilizado e o tempo de sistema, permitindo que os usuários analisem o desempenho de seus scripts e comandos.

## Usage
A sintaxe básica do comando `time` é a seguinte:

```bash
time [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `time`:

- `-p`: Formata a saída de forma mais legível, seguindo o padrão POSIX.
- `-o <arquivo>`: Redireciona a saída do tempo para um arquivo especificado.
- `-v`: Exibe informações detalhadas sobre o tempo de execução.

## Common Examples

### Exemplo 1: Medindo o tempo de um comando simples
```bash
time ls
```
Este comando mede quanto tempo o comando `ls` leva para listar os arquivos no diretório atual.

### Exemplo 2: Usando a opção -p
```bash
time -p sleep 2
```
Aqui, o comando `sleep 2` é executado, e o tempo de execução é exibido em um formato mais legível.

### Exemplo 3: Redirecionando a saída para um arquivo
```bash
time -o tempo.txt wget http://example.com
```
Neste exemplo, o comando `wget` é utilizado para baixar um arquivo, e o tempo de execução é salvo em `tempo.txt`.

### Exemplo 4: Usando a opção -v para detalhes
```bash
time -v find / -name "*.txt"
```
Esse comando procura por arquivos `.txt` em todo o sistema e fornece uma saída detalhada sobre o tempo de execução.

## Tips
- Sempre que possível, use a opção `-p` para uma saída mais clara e fácil de ler.
- Considere redirecionar a saída para um arquivo se você estiver executando comandos longos ou se precisar analisar os resultados mais tarde.
- Use o `time` em scripts para monitorar o desempenho e otimizar comandos que consomem muito tempo.