# [리눅스] Bash foreach 사용법: 반복적으로 명령 실행하기

## Overview
`foreach` 명령은 주어진 리스트의 각 항목에 대해 특정 명령을 반복 실행하는 기능을 제공합니다. 주로 스크립트에서 반복 작업을 수행할 때 유용하게 사용됩니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
foreach [options] [arguments]
```

## Common Options
- `-n`: 각 반복에서 명령을 실행하기 전에 항목을 출력하지 않습니다.
- `-p`: 각 항목에 대해 명령을 실행하기 전에 사용자에게 입력을 요청합니다.

## Common Examples
다음은 `foreach` 명령을 사용하는 몇 가지 예시입니다.

### 예시 1: 파일 목록 출력
```bash
foreach file (file1.txt file2.txt file3.txt)
    echo "Processing $file"
end
```
이 예시는 `file1.txt`, `file2.txt`, `file3.txt` 파일을 반복적으로 처리하는 방법을 보여줍니다.

### 예시 2: 디렉토리 내 모든 파일 삭제
```bash
foreach file (`ls`)
    rm $file
end
```
현재 디렉토리의 모든 파일을 삭제하는 예시입니다.

### 예시 3: 여러 명령 실행
```bash
foreach i (1 2 3)
    echo "Iteration $i"
    sleep 1
end
```
1초 간격으로 1, 2, 3을 출력하는 예시입니다.

## Tips
- `foreach` 명령을 사용할 때는 리스트의 항목이 올바른지 확인하세요.
- 복잡한 작업을 수행할 경우, 스크립트를 작성하여 관리하는 것이 좋습니다.
- 명령 실행 전에 항상 테스트 환경에서 확인하여 실수를 방지하세요.