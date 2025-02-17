# [리눅스] Bash brew 사용법: 패키지 관리 도구

## Overview
`brew` 명령은 macOS 및 Linux에서 소프트웨어 패키지를 쉽게 설치하고 관리할 수 있도록 도와주는 패키지 관리 도구입니다. Homebrew는 사용자가 필요한 소프트웨어를 간편하게 설치하고 업데이트할 수 있게 해줍니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
brew [options] [arguments]
```

## Common Options
- `install`: 지정한 패키지를 설치합니다.
- `uninstall`: 설치된 패키지를 제거합니다.
- `update`: Homebrew와 설치된 패키지 목록을 업데이트합니다.
- `upgrade`: 설치된 패키지를 최신 버전으로 업그레이드합니다.
- `list`: 설치된 모든 패키지를 나열합니다.

## Common Examples
- **패키지 설치**
```bash
brew install wget
```
위 명령은 `wget` 패키지를 설치합니다.

- **패키지 제거**
```bash
brew uninstall wget
```
위 명령은 설치된 `wget` 패키지를 제거합니다.

- **패키지 목록 보기**
```bash
brew list
```
위 명령은 현재 설치된 모든 패키지를 나열합니다.

- **패키지 업데이트**
```bash
brew update
```
위 명령은 Homebrew와 설치된 패키지 목록을 최신 상태로 업데이트합니다.

- **패키지 업그레이드**
```bash
brew upgrade wget
```
위 명령은 `wget` 패키지를 최신 버전으로 업그레이드합니다.

## Tips
- 패키지를 설치하기 전에 `brew update`를 실행하여 최신 패키지 정보를 가져오는 것이 좋습니다.
- 필요하지 않은 패키지는 주기적으로 `brew cleanup` 명령을 사용하여 정리하세요.
- `brew search [package_name]` 명령을 사용하면 설치 가능한 패키지를 검색할 수 있습니다.