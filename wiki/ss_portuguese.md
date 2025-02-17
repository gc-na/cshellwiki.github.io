# [Linux] Bash ss Uso: Exibir informações sobre conexões de rede

## Overview
O comando `ss` é utilizado para investigar e exibir informações sobre conexões de rede no sistema. Ele fornece detalhes sobre sockets, incluindo conexões TCP, UDP e outras, permitindo que os usuários monitorem o estado da rede de maneira eficiente.

## Usage
A sintaxe básica do comando `ss` é a seguinte:

```bash
ss [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do comando `ss`:

- `-t`: Exibe apenas conexões TCP.
- `-u`: Exibe apenas conexões UDP.
- `-l`: Mostra apenas sockets que estão escutando.
- `-p`: Exibe o processo que possui a conexão.
- `-n`: Mostra números de porta e endereços em vez de nomes.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `ss`:

1. **Exibir todas as conexões TCP:**
   ```bash
   ss -t
   ```

2. **Exibir todas as conexões UDP:**
   ```bash
   ss -u
   ```

3. **Exibir todos os sockets em escuta:**
   ```bash
   ss -l
   ```

4. **Exibir conexões com detalhes do processo:**
   ```bash
   ss -p
   ```

5. **Exibir conexões com endereços e portas em formato numérico:**
   ```bash
   ss -n
   ```

## Tips
- Utilize a opção `-s` para obter um resumo das conexões, o que pode ser útil para uma visão geral rápida.
- Combine opções para filtrar resultados, como `ss -tunlp`, que exibe conexões TCP e UDP, sockets em escuta, e detalhes do processo.
- Para uma análise mais detalhada, considere usar `ss` em conjunto com outros comandos de rede, como `netstat` ou `lsof`.