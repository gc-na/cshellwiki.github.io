# [리눅스] Bash pacman 사용법: 패키지 관리 명령어

## Overview
pacman은 Arch Linux 및 그 파생 배포판에서 사용되는 패키지 관리 도구입니다. 이 명령어는 소프트웨어 패키지를 설치, 업데이트, 제거 및 관리하는 데 사용됩니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
pacman [options] [arguments]
```

## Common Options
- `-S`: 패키지를 설치하거나 업데이트합니다.
- `-R`: 패키지를 제거합니다.
- `-U`: 로컬 파일에서 패키지를 설치합니다.
- `-Q`: 설치된 패키지의 정보를 조회합니다.
- `-Sy`: 패키지 데이터베이스를 동기화합니다.

## Common Examples
- 패키지 설치:
```bash
pacman -S package_name
```
- 패키지 제거:
```bash
pacman -R package_name
```
- 로컬 파일에서 패키지 설치:
```bash
pacman -U /path/to/package_file.pkg.tar.zst
```
- 설치된 패키지 목록 조회:
```bash
pacman -Q
```
- 패키지 데이터베이스 동기화:
```bash
pacman -Sy
```

## Tips
- 패키지를 설치하기 전에 항상 데이터베이스를 동기화하는 것이 좋습니다.
- `-Syu` 옵션을 사용하여 시스템을 전체적으로 업데이트할 수 있습니다.
- 패키지를 제거할 때 의존성 문제를 피하기 위해 `-Rns` 옵션을 사용하는 것이 유용합니다.