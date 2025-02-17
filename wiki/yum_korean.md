# [리눅스] Bash yum 사용법: 패키지 관리 명령어

## Overview
`yum`은 리눅스 배포판에서 소프트웨어 패키지를 설치, 업데이트, 삭제 및 관리하는 데 사용되는 패키지 관리 도구입니다. 주로 RPM 기반의 시스템에서 사용되며, 의존성 문제를 자동으로 해결해 주는 기능이 있습니다.

## Usage
`yum` 명령어의 기본 구문은 다음과 같습니다:

```bash
yum [options] [arguments]
```

## Common Options
- `install`: 지정한 패키지를 설치합니다.
- `remove`: 지정한 패키지를 삭제합니다.
- `update`: 설치된 패키지를 최신 버전으로 업데이트합니다.
- `search`: 패키지 이름이나 설명을 검색합니다.
- `list`: 설치된 패키지나 사용 가능한 패키지 목록을 표시합니다.

## Common Examples
- 패키지 설치하기:
    ```bash
    yum install httpd
    ```

- 패키지 삭제하기:
    ```bash
    yum remove httpd
    ```

- 패키지 업데이트하기:
    ```bash
    yum update
    ```

- 특정 패키지 검색하기:
    ```bash
    yum search nginx
    ```

- 설치된 패키지 목록 보기:
    ```bash
    yum list installed
    ```

## Tips
- `yum` 명령어를 사용할 때는 항상 관리자 권한이 필요하므로 `sudo`를 사용하는 것이 좋습니다.
- 패키지를 설치하기 전에 `yum check-update` 명령어로 시스템의 업데이트 상태를 확인하는 것이 유용합니다.
- `yum clean all` 명령어를 사용하여 캐시를 정리하면 디스크 공간을 절약할 수 있습니다.