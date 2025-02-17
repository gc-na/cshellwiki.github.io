# [Linux] Bash helm uso: Manage Kubernetes applications

## Overview
The `helm` command is a package manager for Kubernetes that simplifies the deployment and management of applications on Kubernetes clusters. It allows users to define, install, and upgrade even the most complex Kubernetes applications using Helm charts, which are collections of files that describe a related set of Kubernetes resources.

## Usage
The basic syntax of the helm command is as follows:

```bash
helm [options] [command] [arguments]
```

## Common Options
- `install`: Install a new chart.
- `upgrade`: Upgrade an existing release with a new chart version.
- `uninstall`: Remove a release from the cluster.
- `list`: List all releases in the current namespace.
- `repo`: Manage chart repositories.

## Common Examples
Here are some practical examples of using the helm command:

### Install a Chart
To install a chart (e.g., `nginx`):

```bash
helm install my-nginx stable/nginx
```

### Upgrade a Release
To upgrade an existing release (e.g., `my-nginx`):

```bash
helm upgrade my-nginx stable/nginx
```

### Uninstall a Release
To uninstall a release (e.g., `my-nginx`):

```bash
helm uninstall my-nginx
```

### List Installed Releases
To list all installed releases:

```bash
helm list
```

### Add a Chart Repository
To add a new chart repository (e.g., `bitnami`):

```bash
helm repo add bitnami https://charts.bitnami.com/bitnami
```

## Tips
- Always check the available charts in a repository with `helm search repo [keyword]` to find the right application.
- Use `helm get all [release-name]` to view all information about a specific release.
- Keep your Helm repositories up to date with `helm repo update` to ensure you have the latest charts available.