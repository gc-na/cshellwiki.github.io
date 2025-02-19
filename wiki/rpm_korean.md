# [리눅스] C Shell (csh) rpm 사용법: 패키지 관리 명령어

## Overview
`rpm` 명령어는 Red Hat 계열의 리눅스 배포판에서 소프트웨어 패키지를 관리하기 위해 사용됩니다. 이 명령어를 통해 패키지를 설치, 제거, 업데이트 및 쿼리할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```
rpm [options] [arguments]
```

## Common Options
- `-i` : 패키지를 설치합니다.
- `-e` : 패키지를 제거합니다.
- `-U` : 패키지를 업데이트합니다.
- `-q` : 패키지에 대한 정보를 쿼리합니다.
- `--help` : 사용 가능한 옵션 목록을 표시합니다.

## Common Examples
패키지를 설치하는 예:
```bash
rpm -i package.rpm
```

패키지를 제거하는 예:
```bash
rpm -e package_name
```

패키지를 업데이트하는 예:
```bash
rpm -U package.rpm
```

패키지 정보를 쿼리하는 예:
```bash
rpm -q package_name
```

## Tips
- 패키지를 설치하기 전에 항상 의존성을 확인하세요.
- `--help` 옵션을 사용하여 추가적인 옵션을 확인할 수 있습니다.
- 패키지를 제거하기 전에 해당 패키지가 다른 소프트웨어에 의존하고 있는지 확인하세요.