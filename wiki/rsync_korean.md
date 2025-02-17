# [리눅스] Bash rsync 사용법: 파일 및 디렉토리 동기화

## Overview
`rsync` 명령어는 파일과 디렉토리를 효율적으로 동기화하는 데 사용됩니다. 로컬 및 원격 시스템 간에 데이터를 전송할 수 있으며, 변경된 부분만 전송하여 대역폭을 절약합니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
rsync [options] [source] [destination]
```

## Common Options
- `-a`: 아카이브 모드로, 파일의 소유권, 권한, 심볼릭 링크 등을 유지합니다.
- `-v`: 진행 상황을 자세히 보여줍니다 (verbose).
- `-z`: 전송 중 데이터를 압축하여 대역폭을 절약합니다.
- `-r`: 하위 디렉토리를 재귀적으로 복사합니다.
- `--delete`: 대상 디렉토리에서 소스에 없는 파일을 삭제합니다.

## Common Examples
1. 로컬 디렉토리 복사:
   ```bash
   rsync -av /path/to/source/ /path/to/destination/
   ```

2. 원격 서버로 파일 전송:
   ```bash
   rsync -av /path/to/local/file user@remote_host:/path/to/remote/destination/
   ```

3. 원격 서버에서 로컬로 파일 다운로드:
   ```bash
   rsync -av user@remote_host:/path/to/remote/file /path/to/local/destination/
   ```

4. 변경된 파일만 동기화:
   ```bash
   rsync -av --update /path/to/source/ /path/to/destination/
   ```

5. 원격 서버의 파일 삭제:
   ```bash
   rsync -av --delete /path/to/source/ user@remote_host:/path/to/remote/destination/
   ```

## Tips
- `--dry-run` 옵션을 사용하여 실제 전송 전에 어떤 파일이 전송될지를 미리 확인할 수 있습니다.
- 대용량 파일 전송 시 `-z` 옵션을 사용하여 전송 속도를 개선할 수 있습니다.
- 주기적으로 백업을 수행할 경우, cron 작업을 설정하여 자동화할 수 있습니다.