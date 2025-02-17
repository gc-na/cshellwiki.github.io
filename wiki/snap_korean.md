# [리눅스] Bash snap 사용법: 패키지 관리 및 설치

## Overview
`snap` 명령은 리눅스 시스템에서 소프트웨어 패키지를 설치, 업데이트 및 관리하는 데 사용됩니다. Snap 패키지는 의존성을 포함하고 있어 다양한 리눅스 배포판에서 일관되게 작동합니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
snap [options] [arguments]
```

## Common Options
- `install`: 패키지를 설치합니다.
- `remove`: 설치된 패키지를 제거합니다.
- `list`: 설치된 패키지 목록을 표시합니다.
- `refresh`: 설치된 패키지를 업데이트합니다.
- `info`: 특정 패키지에 대한 정보를 표시합니다.

## Common Examples
- **패키지 설치하기**
  ```bash
  snap install vlc
  ```
  VLC 미디어 플레이어를 설치합니다.

- **패키지 제거하기**
  ```bash
  snap remove vlc
  ```
  설치된 VLC 미디어 플레이어를 제거합니다.

- **설치된 패키지 목록 보기**
  ```bash
  snap list
  ```
  현재 설치된 모든 snap 패키지의 목록을 표시합니다.

- **패키지 업데이트하기**
  ```bash
  snap refresh
  ```
  모든 설치된 snap 패키지를 최신 버전으로 업데이트합니다.

- **특정 패키지 정보 보기**
  ```bash
  snap info vlc
  ```
  VLC 패키지에 대한 상세 정보를 표시합니다.

## Tips
- Snap 패키지는 자동으로 업데이트되므로, 최신 기능을 항상 사용할 수 있습니다.
- `snap` 명령은 루트 권한이 필요하지 않지만, 특정 패키지에 따라 권한이 필요할 수 있습니다.
- 패키지 설치 후, `snap list` 명령을 사용하여 설치된 패키지를 확인하는 것이 좋습니다.