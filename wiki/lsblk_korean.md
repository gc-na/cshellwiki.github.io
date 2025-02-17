# [리눅스] Bash lsblk 사용법: 블록 장치 목록 보기

## Overview
`lsblk` 명령어는 시스템에 연결된 블록 장치의 목록을 출력하는 데 사용됩니다. 이 명령어는 각 장치의 크기, 유형, 마운트 지점 등을 보여주어 시스템의 저장 장치 구조를 이해하는 데 도움을 줍니다.

## Usage
기본 구문은 다음과 같습니다:
```bash
lsblk [options] [arguments]
```

## Common Options
- `-a`, `--all`: 모든 장치를 표시합니다. 마운트되지 않은 장치도 포함됩니다.
- `-f`, `--fs`: 파일 시스템 정보를 함께 표시합니다.
- `-l`, `--list`: 리스트 형식으로 출력합니다.
- `-o`, `--output`: 출력할 열을 지정합니다.
- `-p`, `--paths`: 장치의 전체 경로를 표시합니다.

## Common Examples
- 기본 블록 장치 목록 보기:
    ```bash
    lsblk
    ```

- 모든 장치 및 마운트되지 않은 장치 포함:
    ```bash
    lsblk -a
    ```

- 파일 시스템 정보와 함께 보기:
    ```bash
    lsblk -f
    ```

- 리스트 형식으로 출력하기:
    ```bash
    lsblk -l
    ```

- 특정 열만 출력하기 (예: NAME, SIZE, FSTYPE):
    ```bash
    lsblk -o NAME,SIZE,FSTYPE
    ```

## Tips
- `lsblk` 명령어는 `sudo`와 함께 사용하여 더 많은 정보를 얻을 수 있습니다.
- 출력 결과를 `grep`과 함께 사용하여 특정 장치를 쉽게 찾을 수 있습니다. 예를 들어, 특정 이름을 가진 장치를 찾으려면:
    ```bash
    lsblk | grep sda
    ```
- `lsblk`의 출력 결과를 파일로 저장하려면 리다이렉션을 사용할 수 있습니다:
    ```bash
    lsblk > 블록장치목록.txt
    ```