# [리눅스] Bash mtr 사용법: 네트워크 경로 추적

## Overview
mtr (My Traceroute) 명령어는 네트워크 경로를 추적하고, 패킷 손실 및 지연 시간을 측정하여 네트워크 성능을 분석하는 도구입니다. 이 명령어는 traceroute와 ping의 기능을 결합하여 실시간으로 네트워크 상태를 모니터링할 수 있습니다.

## Usage
mtr 명령어의 기본 구문은 다음과 같습니다.

```bash
mtr [options] [arguments]
```

## Common Options
- `-r`: 보고서 모드로 실행하여 결과를 한 번만 출력합니다.
- `-c <count>`: 지정된 횟수만큼 패킷을 전송합니다.
- `-i <interval>`: 패킷 전송 간격을 설정합니다.
- `-p`: 포트 번호를 지정하여 특정 포트에 대해 테스트합니다.
- `-n`: IP 주소를 숫자로만 표시하여 DNS 조회를 생략합니다.

## Common Examples
1. 기본적인 mtr 사용법:
   ```bash
   mtr google.com
   ```

2. 특정 횟수만큼 패킷 전송하기:
   ```bash
   mtr -c 10 google.com
   ```

3. 보고서 모드로 실행하기:
   ```bash
   mtr -r google.com
   ```

4. 패킷 전송 간격 설정하기:
   ```bash
   mtr -i 0.5 google.com
   ```

5. 특정 포트에 대해 테스트하기:
   ```bash
   mtr -p 80 google.com
   ```

## Tips
- mtr를 실행할 때, 관리자 권한이 필요할 수 있으므로 `sudo`를 사용하는 것이 좋습니다.
- 결과를 분석할 때, 패킷 손실이 발생하는 노드를 주의 깊게 살펴보세요.
- mtr의 출력을 CSV 형식으로 저장하여 후속 분석에 활용할 수 있습니다.