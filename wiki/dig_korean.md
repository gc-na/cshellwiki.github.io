# [리눅스] C Shell (csh) dig 사용법: DNS 조회 도구

## Overview
`dig` 명령어는 도메인 이름 시스템(DNS) 정보를 조회하는 데 사용되는 도구입니다. 이 명령어를 통해 도메인 이름에 대한 IP 주소, MX 레코드, NS 레코드 등 다양한 정보를 쉽게 확인할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```
dig [옵션] [인수]
```

## Common Options
- `@서버`: 특정 DNS 서버에 쿼리를 보냅니다.
- `-t 타입`: 조회할 레코드의 타입을 지정합니다 (예: A, AAAA, MX 등).
- `+short`: 간단한 출력 형식으로 결과를 표시합니다.
- `+trace`: DNS 쿼리의 경로를 추적합니다.

## Common Examples
- 기본 A 레코드 조회:
```bash
dig example.com
```

- 특정 DNS 서버에 쿼리 보내기:
```bash
dig @8.8.8.8 example.com
```

- MX 레코드 조회:
```bash
dig -t MX example.com
```

- 간단한 출력 형식으로 A 레코드 조회:
```bash
dig +short example.com
```

- DNS 쿼리 경로 추적:
```bash
dig +trace example.com
```

## Tips
- `dig` 명령어는 DNS 문제를 진단하는 데 유용하므로, 네트워크 문제가 발생했을 때 자주 사용됩니다.
- 여러 레코드 타입을 조회할 수 있으므로, 필요한 정보를 정확히 지정하는 것이 좋습니다.
- 결과를 스크립트에서 활용할 경우, `+short` 옵션을 사용하여 출력 형식을 간단하게 유지하는 것이 유용합니다.