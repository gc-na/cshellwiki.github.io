# [리눅스] Bash zypper 사용법: 패키지 관리 명령어

## Overview
`zypper`는 openSUSE 및 SUSE Linux Enterprise에서 사용되는 패키지 관리 도구입니다. 이 명령어는 소프트웨어 패키지를 설치, 업데이트, 제거 및 관리하는 데 사용됩니다.

## Usage
기본 구문은 다음과 같습니다:
```
zypper [options] [arguments]
```

## Common Options
- `install`: 패키지를 설치합니다.
- `remove`: 패키지를 제거합니다.
- `update`: 설치된 패키지를 업데이트합니다.
- `search`: 패키지를 검색합니다.
- `info`: 패키지에 대한 정보를 표시합니다.

## Common Examples
- 패키지 설치:
  ```bash
  zypper install vim
  ```
- 패키지 제거:
  ```bash
  zypper remove vim
  ```
- 패키지 업데이트:
  ```bash
  zypper update
  ```
- 패키지 검색:
  ```bash
  zypper search nginx
  ```
- 패키지 정보 보기:
  ```bash
  zypper info vim
  ```

## Tips
- 패키지를 설치하기 전에 항상 `zypper refresh` 명령어로 저장소 정보를 업데이트하는 것이 좋습니다.
- `zypper up` 명령어를 사용하여 시스템의 모든 패키지를 한 번에 업데이트할 수 있습니다.
- 특정 패키지의 의존성을 확인하려면 `zypper info [패키지명]`을 사용하세요.