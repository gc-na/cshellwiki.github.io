# [리눅스] Bash 스크립트 사용법: 터미널 세션 기록하기

## Overview
`script` 명령은 사용자가 터미널에서 수행하는 모든 작업을 기록하는 데 사용됩니다. 이 명령은 주로 세션을 기록하고 나중에 재검토할 수 있도록 하는 데 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```
script [options] [file]
```

## Common Options
- `-a`: 기존 파일에 추가하여 기록합니다.
- `-c`: 특정 명령을 실행하고 그 출력을 기록합니다.
- `-f`: 출력 내용을 실시간으로 표시합니다.
- `-q`: 기록 중에 출력하지 않습니다.

## Common Examples
1. 기본 사용법으로 세션 기록하기:
   ```bash
   script mysession.txt
   ```
   이 명령은 `mysession.txt` 파일에 세션을 기록합니다.

2. 특정 명령의 출력을 기록하기:
   ```bash
   script -c "ls -l" output.txt
   ```
   이 명령은 `ls -l` 명령의 출력을 `output.txt` 파일에 기록합니다.

3. 기존 파일에 추가하여 기록하기:
   ```bash
   script -a mysession.txt
   ```
   이 명령은 기존의 `mysession.txt` 파일에 추가하여 기록합니다.

4. 실시간으로 출력 보기:
   ```bash
   script -f mysession.txt
   ```
   이 명령은 세션을 기록하면서 실시간으로 출력을 표시합니다.

## Tips
- 기록을 시작하기 전에 세션을 정리해 두면 나중에 검토할 때 더 유용합니다.
- `script` 명령을 사용할 때, 기록된 파일을 쉽게 찾을 수 있도록 명확한 파일 이름을 사용하는 것이 좋습니다.
- 세션을 종료하려면 `exit` 명령을 입력하면 됩니다.