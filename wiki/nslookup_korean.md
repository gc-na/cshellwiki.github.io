# [리눅스] Bash nslookup 사용법: 도메인 이름을 IP 주소로 변환

## Overview
`nslookup` 명령어는 도메인 이름 시스템(DNS)에서 도메인 이름을 IP 주소로 변환하거나 그 반대의 작업을 수행하는 도구입니다. 이 명령어는 네트워크 문제를 진단하고 DNS 레코드를 조회하는 데 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```
nslookup [옵션] [인수]
```

## Common Options
- `-type=TYPE`: 조회할 DNS 레코드의 유형을 지정합니다. 예: A, AAAA, MX 등.
- `-timeout=SECONDS`: 응답 대기 시간을 설정합니다.
- `-retry=COUNT`: 요청 실패 시 재시도 횟수를 설정합니다.

## Common Examples
1. 기본 도메인 이름 조회:
   ```bash
   nslookup example.com
   ```

2. 특정 DNS 서버를 사용하여 조회:
   ```bash
   nslookup example.com 8.8.8.8
   ```

3. MX 레코드 조회:
   ```bash
   nslookup -type=MX example.com
   ```

4. AAAA 레코드 조회 (IPv6 주소):
   ```bash
   nslookup -type=AAAA example.com
   ```

## Tips
- DNS 문제를 해결할 때 `nslookup`을 사용하여 다양한 DNS 서버에서 결과를 비교해 보세요.
- `-debug` 옵션을 사용하면 더 자세한 정보를 얻을 수 있어 문제를 진단하는 데 도움이 됩니다.
- 도메인 이름과 IP 주소 간의 변환을 자주 수행해야 한다면 스크립트를 작성하여 자동화할 수 있습니다.