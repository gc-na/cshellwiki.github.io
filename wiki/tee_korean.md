# [리눅스] Bash tee 사용법: 표준 입력을 파일에 저장하고 출력하기

## Overview
`tee` 명령어는 표준 입력을 파일에 저장하면서 동시에 표준 출력을 통해 데이터를 출력하는 기능을 제공합니다. 이 명령어는 파이프라인에서 데이터를 처리할 때 유용하게 사용됩니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
tee [옵션] [파일명]
```

## Common Options
- `-a`, `--append`: 파일에 데이터를 추가합니다. 기본적으로는 파일을 덮어씁니다.
- `-i`, `--ignore-interrupts`: 인터럽트 신호를 무시합니다.
- `--help`: 사용법을 출력합니다.
- `--version`: 버전 정보를 출력합니다.

## Common Examples
1. **파일에 출력 저장하기**
   ```bash
   echo "Hello, World!" | tee output.txt
   ```
   이 명령어는 "Hello, World!"라는 문자열을 `output.txt` 파일에 저장하고, 동시에 터미널에도 출력합니다.

2. **파일에 추가하기**
   ```bash
   echo "Another line" | tee -a output.txt
   ```
   이 명령어는 `output.txt` 파일에 "Another line"을 추가하고, 터미널에도 출력합니다.

3. **여러 파일에 출력하기**
   ```bash
   echo "Logging data" | tee file1.txt file2.txt
   ```
   이 명령어는 "Logging data"를 `file1.txt`와 `file2.txt` 두 파일에 저장하고, 동시에 터미널에 출력합니다.

4. **명령어의 출력 저장하기**
   ```bash
   ls -l | tee directory_list.txt
   ```
   이 명령어는 현재 디렉토리의 파일 목록을 `directory_list.txt` 파일에 저장하고, 터미널에도 출력합니다.

## Tips
- `tee`를 사용할 때 `-a` 옵션을 활용하여 기존 파일에 데이터를 추가할 수 있습니다.
- 파이프라인에서 여러 명령어와 함께 사용하여 중간 결과를 파일에 저장하면서 전체 흐름을 유지할 수 있습니다.
- `tee` 명령어는 스크립트에서 로그를 기록할 때 유용하게 사용됩니다.