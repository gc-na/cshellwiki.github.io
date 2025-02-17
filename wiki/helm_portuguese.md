# [Linux] Bash helm uso: Gerenciar gráficos do Kubernetes

## Overview
O comando `helm` é uma ferramenta de gerenciamento de pacotes para Kubernetes, que permite instalar, atualizar e gerenciar aplicativos em clusters Kubernetes de forma eficiente. Ele utiliza gráficos (charts) que são pacotes de configuração que contêm todos os recursos necessários para executar uma aplicação.

## Usage
A sintaxe básica do comando `helm` é a seguinte:

```bash
helm [options] [arguments]
```

## Common Options
Aqui estão algumas opções comuns do `helm`:

- `install`: Instala um gráfico em um cluster Kubernetes.
- `upgrade`: Atualiza um gráfico já instalado.
- `uninstall`: Remove um gráfico do cluster.
- `list`: Lista os gráficos instalados no cluster.
- `repo`: Gerencia repositórios de gráficos.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `helm`:

### Instalar um gráfico
Para instalar um gráfico chamado `meu-app` a partir do repositório padrão:

```bash
helm install meu-app stable/meu-app
```

### Atualizar um gráfico
Para atualizar um gráfico já instalado chamado `meu-app`:

```bash
helm upgrade meu-app stable/meu-app
```

### Desinstalar um gráfico
Para remover um gráfico chamado `meu-app` do cluster:

```bash
helm uninstall meu-app
```

### Listar gráficos instalados
Para listar todos os gráficos instalados no seu cluster:

```bash
helm list
```

### Adicionar um repositório de gráficos
Para adicionar um novo repositório de gráficos:

```bash
helm repo add meu-repo https://meu-repo-url.com
```

## Tips
- Sempre verifique a documentação do gráfico que você está instalando para entender suas dependências e configurações.
- Utilize `helm search` para encontrar gráficos disponíveis em repositórios.
- Mantenha seus repositórios atualizados com `helm repo update` para garantir que você tenha as versões mais recentes dos gráficos.