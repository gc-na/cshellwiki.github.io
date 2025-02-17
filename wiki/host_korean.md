# [리눅스] Bash host 사용법: DNS 쿼리 도구

## Overview
`host` 명령어는 도메인 이름을 IP 주소로 변환하거나 그 반대로 변환하는 DNS 쿼리 도구입니다. 이 명령어는 DNS 정보를 조회하고, 특정 도메인에 대한 레코드를 확인하는 데 유용합니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
host [옵션] [도메인 이름] [서버]
```

## Common Options
- `-a`: 모든 레코드 타입을 조회합니다.
- `-t TYPE`: 특정 레코드 타입을 지정하여 조회합니다. (예: A, MX, TXT 등)
- `-v`: 자세한 출력을 제공합니다.
- `-W TIMEOUT`: 응답 대기 시간을 설정합니다.

## Common Examples
- 특정 도메인의 IP 주소 조회:
  ```bash
  host example.com
  ```

- 특정 도메인의 MX 레코드 조회:
  ```bash
  host -t MX example.com
  ```

- 특정 DNS 서버를 사용하여 도메인 조회:
  ```bash
  host example.com 8.8.8.8
  ```

- 모든 레코드 타입 조회:
  ```bash
  host -a example.com
  ```

## Tips
- DNS 문제를 해결할 때 `-v` 옵션을 사용하여 더 많은 정보를 얻을 수 있습니다.
- 여러 도메인에 대한 정보를 한 번에 조회하려면 스크립트를 작성하여 반복적으로 `host` 명령어를 사용할 수 있습니다.
- DNS 캐시를 확인하고 싶다면 `dig` 명령어도 함께 사용하는 것이 좋습니다.