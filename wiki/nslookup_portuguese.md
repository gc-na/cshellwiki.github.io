# [Linux] Bash nslookup Uso: Consulta de DNS

## Overview
O comando `nslookup` é uma ferramenta de linha de comando utilizada para consultar informações sobre servidores de nomes de domínio (DNS). Ele permite que os usuários obtenham detalhes sobre endereços IP, registros de domínio e outros dados relacionados a DNS.

## Usage
A sintaxe básica do comando `nslookup` é a seguinte:

```bash
nslookup [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `nslookup`:

- `-type=tipo`: Especifica o tipo de registro DNS a ser consultado (por exemplo, A, AAAA, MX, etc.).
- `-timeout=segundos`: Define o tempo limite para a consulta DNS.
- `-retry=número`: Define o número de tentativas de consulta em caso de falha.
- `-debug`: Ativa o modo de depuração para exibir informações detalhadas sobre a consulta.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `nslookup`:

1. **Consultar o endereço IP de um domínio:**

```bash
nslookup exemplo.com
```

2. **Consultar um registro específico (por exemplo, MX):**

```bash
nslookup -type=MX exemplo.com
```

3. **Alterar o servidor DNS para a consulta:**

```bash
nslookup exemplo.com 8.8.8.8
```

4. **Ativar o modo de depuração:**

```bash
nslookup -debug exemplo.com
```

## Tips
- Sempre verifique se você está usando o servidor DNS correto, especialmente ao solucionar problemas de conectividade.
- Utilize a opção `-type` para obter informações específicas que você precisa, evitando resultados desnecessários.
- O modo de depuração é útil para entender o que está acontecendo durante a consulta, especialmente em casos de falhas.