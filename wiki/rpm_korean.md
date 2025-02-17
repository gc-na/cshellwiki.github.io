# [리눅스] Bash rpm 사용법: 패키지 관리 명령어

## Overview
`rpm` 명령어는 리눅스에서 소프트웨어 패키지를 관리하는 데 사용됩니다. 이 명령어는 패키지를 설치, 제거, 업그레이드 및 검증하는 기능을 제공합니다. RPM(Red Hat Package Manager) 형식의 패키지를 다루는 데 최적화되어 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
rpm [options] [arguments]
```

## Common Options
- `-i`: 패키지를 설치합니다.
- `-e`: 패키지를 제거합니다.
- `-U`: 패키지를 업그레이드합니다.
- `-q`: 패키지 정보를 조회합니다.
- `-V`: 패키지의 무결성을 검증합니다.

## Common Examples
- 패키지 설치:
```bash
rpm -i package.rpm
```

- 패키지 제거:
```bash
rpm -e package_name
```

- 패키지 업그레이드:
```bash
rpm -U package.rpm
```

- 설치된 패키지 목록 조회:
```bash
rpm -qa
```

- 특정 패키지 정보 조회:
```bash
rpm -q package_name
```

- 패키지 무결성 검증:
```bash
rpm -V package_name
```

## Tips
- 패키지를 설치하기 전에 항상 의존성을 확인하세요.
- `-q` 옵션을 사용하여 설치된 패키지의 버전을 확인할 수 있습니다.
- RPM 패키지를 설치할 때는 `--force` 옵션을 사용하여 강제로 설치할 수 있지만, 주의가 필요합니다.