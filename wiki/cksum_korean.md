# [리눅스] Bash cksum 사용법: 파일의 체크섬 계산

## Overview
`cksum` 명령어는 파일의 체크섬과 바이트 수를 계산하여 출력하는 도구입니다. 체크섬은 파일의 무결성을 확인하는 데 사용되며, 파일이 손상되었는지 여부를 판단하는 데 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```
cksum [options] [arguments]
```

## Common Options
- `-a, --algorithm`: 체크섬 알고리즘을 지정합니다.
- `-h, --help`: 도움말 메시지를 출력합니다.
- `-V, --version`: 버전 정보를 출력합니다.

## Common Examples
1. **단일 파일의 체크섬 계산**
   ```bash
   cksum myfile.txt
   ```
   이 명령어는 `myfile.txt`의 체크섬과 바이트 수를 출력합니다.

2. **여러 파일의 체크섬 계산**
   ```bash
   cksum file1.txt file2.txt
   ```
   이 명령어는 `file1.txt`와 `file2.txt`의 체크섬을 동시에 계산합니다.

3. **체크섬 알고리즘 지정**
   ```bash
   cksum -a md5 myfile.txt
   ```
   이 명령어는 `myfile.txt`의 MD5 체크섬을 계산합니다.

## Tips
- 체크섬을 저장해 두고 나중에 파일의 무결성을 확인할 때 유용합니다.
- 파일을 전송한 후 체크섬을 비교하여 데이터 손실 여부를 확인할 수 있습니다.
- 여러 파일의 체크섬을 한 번에 계산하여 관리할 수 있습니다.