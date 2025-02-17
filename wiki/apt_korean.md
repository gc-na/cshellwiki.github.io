# [리눅스] Bash apt 사용법: 패키지 관리 명령어

## Overview
`apt`는 Debian 및 Ubuntu 기반의 리눅스 배포판에서 소프트웨어 패키지를 관리하는 데 사용되는 명령어입니다. 이 명령어를 통해 패키지를 설치, 업데이트 및 제거할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
apt [options] [arguments]
```

## Common Options
- `install`: 지정한 패키지를 설치합니다.
- `remove`: 지정한 패키지를 제거합니다.
- `update`: 패키지 목록을 업데이트합니다.
- `upgrade`: 설치된 모든 패키지를 최신 버전으로 업그레이드합니다.
- `search`: 패키지 이름이나 설명을 검색합니다.

## Common Examples
- 패키지 목록 업데이트:
  ```bash
  sudo apt update
  ```
  
- 특정 패키지 설치:
  ```bash
  sudo apt install vim
  ```

- 패키지 제거:
  ```bash
  sudo apt remove vim
  ```

- 모든 패키지 업그레이드:
  ```bash
  sudo apt upgrade
  ```

- 패키지 검색:
  ```bash
  apt search nginx
  ```

## Tips
- `sudo`를 사용하여 관리자 권한으로 명령을 실행하세요.
- `apt` 명령어를 사용할 때는 항상 `update`를 먼저 실행하여 최신 패키지 정보를 가져오는 것이 좋습니다.
- 패키지를 설치하기 전에 `apt-cache show [패키지명]` 명령어로 패키지의 정보를 확인할 수 있습니다.