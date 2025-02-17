# [리눅스] Bash hexdump 사용법: 파일의 헥사 덤프 출력

## Overview
hexdump 명령어는 파일의 내용을 헥사(16진수) 형식으로 출력하는 데 사용됩니다. 이 명령어는 바이너리 파일을 분석하거나 디버깅할 때 유용합니다.

## Usage
hexdump의 기본 구문은 다음과 같습니다.

```bash
hexdump [options] [arguments]
```

## Common Options
- `-C`: 헥사 덤프와 ASCII 출력을 함께 보여줍니다.
- `-n <number>`: 출력할 바이트 수를 지정합니다.
- `-v`: 모든 데이터를 출력하며, 중복된 바이트도 표시합니다.
- `-e <format>`: 사용자 지정 형식으로 출력을 설정합니다.

## Common Examples
1. **기본 헥사 덤프 출력**
   ```bash
   hexdump example.txt
   ```

2. **헥사 덤프와 ASCII 출력**
   ```bash
   hexdump -C example.txt
   ```

3. **특정 바이트 수만 출력**
   ```bash
   hexdump -n 16 example.txt
   ```

4. **사용자 지정 형식으로 출력**
   ```bash
   hexdump -e '16/1 "%02x " "\n"' example.txt
   ```

5. **모든 데이터 출력**
   ```bash
   hexdump -v example.txt
   ```

## Tips
- 헥사 덤프를 분석할 때, `-C` 옵션을 사용하면 헥사 값과 ASCII 값을 동시에 확인할 수 있어 유용합니다.
- 큰 파일을 다룰 때는 `-n` 옵션으로 필요한 바이트 수만 출력하여 가독성을 높일 수 있습니다.
- 특정 형식으로 출력할 필요가 있을 경우, `-e` 옵션을 활용하여 원하는 형식으로 데이터를 조정할 수 있습니다.