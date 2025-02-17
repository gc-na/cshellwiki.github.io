# [리눅스] Bash dpkg 사용법: 패키지 관리 명령어

## Overview
`dpkg`는 Debian 및 그 파생 배포판에서 소프트웨어 패키지를 관리하는 데 사용되는 명령어입니다. 이 명령어는 패키지 설치, 제거, 정보 조회 등을 수행할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
dpkg [options] [arguments]
```

## Common Options
- `-i`, `--install`: 지정된 .deb 패키지를 설치합니다.
- `-r`, `--remove`: 설치된 패키지를 제거합니다.
- `-l`, `--list`: 설치된 패키지 목록을 표시합니다.
- `-s`, `--status`: 특정 패키지의 상태 정보를 보여줍니다.
- `-P`, `--purge`: 패키지를 제거하고 관련 설정 파일도 삭제합니다.

## Common Examples
- 패키지 설치:
```bash
sudo dpkg -i package.deb
```
- 패키지 제거:
```bash
sudo dpkg -r package_name
```
- 설치된 패키지 목록 보기:
```bash
dpkg -l
```
- 특정 패키지 상태 확인:
```bash
dpkg -s package_name
```
- 패키지 강제 제거 (설정 파일 포함):
```bash
sudo dpkg -P package_name
```

## Tips
- 패키지를 설치할 때 의존성 문제를 피하기 위해 `apt` 명령어를 사용하는 것이 좋습니다.
- `dpkg`로 패키지를 설치한 후에는 `apt-get install -f`를 사용하여 누락된 의존성을 자동으로 설치할 수 있습니다.
- 패키지의 설치 경로를 알고 싶다면 `dpkg -L package_name` 명령어를 사용하세요.