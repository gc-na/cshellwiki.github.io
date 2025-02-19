# [리눅스] C Shell (csh) yum 사용법: 패키지 관리 명령어

## Overview
`yum`은 Red Hat 계열의 리눅스 배포판에서 패키지를 설치, 업데이트 및 제거하는 데 사용되는 명령어입니다. 이 명령어는 의존성 문제를 자동으로 해결해 주어, 소프트웨어 관리가 간편해집니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
yum [options] [arguments]
```

## Common Options
- `install`: 패키지를 설치합니다.
- `remove`: 패키지를 제거합니다.
- `update`: 설치된 패키지를 업데이트합니다.
- `list`: 사용 가능한 패키지 목록을 보여줍니다.
- `search`: 특정 패키지를 검색합니다.

## Common Examples
패키지를 설치하는 예:
```bash
yum install httpd
```

패키지를 제거하는 예:
```bash
yum remove httpd
```

설치된 패키지를 업데이트하는 예:
```bash
yum update httpd
```

사용 가능한 패키지 목록을 보여주는 예:
```bash
yum list available
```

특정 패키지를 검색하는 예:
```bash
yum search nginx
```

## Tips
- 패키지를 설치하기 전에 항상 `yum list`를 사용하여 패키지가 존재하는지 확인하세요.
- `yum update`를 정기적으로 실행하여 시스템을 최신 상태로 유지하세요.
- `yum clean all` 명령어를 사용하여 캐시를 정리하면 디스크 공간을 절약할 수 있습니다.