# [리눅스] C Shell (csh) mtr 사용법: 네트워크 경로 추적 및 진단

## Overview
mtr (My Traceroute) 명령어는 네트워크 경로를 추적하고, 패킷 손실 및 지연 시간을 측정하는 도구입니다. 이 명령어는 traceroute와 ping의 기능을 결합하여, 네트워크 문제를 진단하는 데 유용합니다.

## Usage
mtr 명령어의 기본 구문은 다음과 같습니다.

```csh
mtr [options] [arguments]
```

## Common Options
- `-r`: 보고서 모드로 실행하여 결과를 요약합니다.
- `-c <count>`: 지정된 수의 패킷을 전송합니다.
- `-i <interval>`: 패킷 전송 간격을 설정합니다.
- `-p`: 포트 번호를 지정하여 특정 포트에 대해 테스트합니다.

## Common Examples
다음은 mtr 명령어의 몇 가지 일반적인 사용 예입니다.

1. 기본 사용법:
   ```csh
   mtr google.com
   ```

2. 10개의 패킷을 전송하는 경우:
   ```csh
   mtr -c 10 google.com
   ```

3. 보고서 모드로 실행하는 경우:
   ```csh
   mtr -r google.com
   ```

4. 특정 포트에 대해 테스트하는 경우:
   ```csh
   mtr -p 80 google.com
   ```

## Tips
- mtr 명령어를 실행할 때, 관리자 권한으로 실행하면 더 많은 정보를 얻을 수 있습니다.
- 네트워크 문제를 진단할 때, 여러 목적지에 대해 mtr을 실행하여 패턴을 확인하는 것이 좋습니다.
- 결과를 저장하려면, 출력 결과를 파일로 리다이렉션할 수 있습니다. 예를 들어:
  ```csh
  mtr google.com > mtr_output.txt
  ```