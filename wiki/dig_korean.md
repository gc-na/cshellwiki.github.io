# [리눅스] Bash dig 사용법: DNS 쿼리 도구

## Overview
`dig` 명령어는 DNS(도메인 네임 시스템) 쿼리를 수행하는 도구로, 도메인 이름에 대한 정보를 조회할 수 있습니다. 이 명령어는 DNS 서버와의 상호작용을 통해 IP 주소, MX 레코드, NS 레코드 등 다양한 정보를 제공합니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
dig [옵션] [인수]
```

## Common Options
- `@server`: 특정 DNS 서버에 쿼리를 보냅니다.
- `-t type`: 요청할 레코드의 유형을 지정합니다 (예: A, MX, NS 등).
- `+short`: 결과를 간단하게 출력합니다.
- `-x`: IP 주소에 대한 역방향 조회를 수행합니다.

## Common Examples
1. **기본 A 레코드 조회**
   ```bash
   dig example.com
   ```

2. **특정 DNS 서버에 쿼리**
   ```bash
   dig @8.8.8.8 example.com
   ```

3. **MX 레코드 조회**
   ```bash
   dig -t MX example.com
   ```

4. **IP 주소에 대한 역방향 조회**
   ```bash
   dig -x 8.8.8.8
   ```

5. **간단한 출력 형식으로 조회**
   ```bash
   dig +short example.com
   ```

## Tips
- DNS 문제를 해결할 때 `dig`를 사용하면 문제의 원인을 쉽게 파악할 수 있습니다.
- `+trace` 옵션을 사용하면 DNS 쿼리의 전체 경로를 추적할 수 있습니다.
- 여러 레코드 유형을 한 번에 조회하려면 `-t ANY`를 사용할 수 있습니다.