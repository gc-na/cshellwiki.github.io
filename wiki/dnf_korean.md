# [리눅스] Bash dnf 사용법: 패키지 관리 명령어

## Overview
`dnf`는 Fedora 및 Red Hat 계열의 리눅스 배포판에서 사용되는 패키지 관리 도구입니다. 소프트웨어 패키지를 설치, 업데이트, 제거 및 관리하는 데 사용됩니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
dnf [options] [arguments]
```

## Common Options
- `install`: 패키지를 설치합니다.
- `remove`: 패키지를 제거합니다.
- `update`: 설치된 패키지를 업데이트합니다.
- `search`: 패키지를 검색합니다.
- `list`: 설치된 패키지 목록을 보여줍니다.
- `info`: 특정 패키지에 대한 정보를 표시합니다.

## Common Examples
- 패키지 설치:
  ```bash
  dnf install package_name
  ```
- 패키지 제거:
  ```bash
  dnf remove package_name
  ```
- 패키지 업데이트:
  ```bash
  dnf update package_name
  ```
- 모든 패키지 업데이트:
  ```bash
  dnf update
  ```
- 패키지 검색:
  ```bash
  dnf search package_name
  ```
- 설치된 패키지 목록 보기:
  ```bash
  dnf list installed
  ```
- 특정 패키지 정보 보기:
  ```bash
  dnf info package_name
  ```

## Tips
- 패키지를 설치하기 전에 항상 `dnf search`를 사용하여 패키지가 존재하는지 확인하세요.
- `dnf update`를 정기적으로 실행하여 시스템을 최신 상태로 유지하세요.
- `dnf` 명령어에 `-y` 옵션을 추가하면 모든 질문에 자동으로 'yes'로 응답합니다. 예: `dnf install -y package_name`.