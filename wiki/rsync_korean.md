# [리눅스] C Shell (csh) rsync 사용법: 파일 및 디렉터리 동기화

## Overview
rsync는 파일과 디렉터리를 효율적으로 동기화하고 전송하는 데 사용되는 명령어입니다. 로컬 및 원격 시스템 간에 데이터를 복사할 수 있으며, 변경된 부분만 전송하여 대역폭을 절약합니다.

## Usage
기본 구문은 다음과 같습니다:
```csh
rsync [options] [arguments]
```

## Common Options
- `-a`: 아카이브 모드로, 파일의 소유권, 권한, 타임스탬프 등을 유지합니다.
- `-v`: 진행 상황을 자세히 출력합니다.
- `-z`: 전송 중 데이터를 압축하여 대역폭을 절약합니다.
- `-r`: 하위 디렉터리를 재귀적으로 복사합니다.
- `--delete`: 대상에서 소스에 없는 파일을 삭제합니다.

## Common Examples
- 로컬 디렉터리 동기화:
```csh
rsync -av /source/directory/ /destination/directory/
```

- 원격 서버로 파일 전송:
```csh
rsync -av /local/file.txt user@remote_host:/remote/directory/
```

- 원격 서버에서 로컬로 파일 다운로드:
```csh
rsync -av user@remote_host:/remote/file.txt /local/directory/
```

- 압축을 사용하여 대량의 파일 전송:
```csh
rsync -avz /source/directory/ user@remote_host:/remote/directory/
```

- 삭제 옵션을 사용하여 동기화:
```csh
rsync -av --delete /source/directory/ /destination/directory/
```

## Tips
- rsync를 사용할 때는 항상 소스와 대상 경로의 끝에 슬래시(`/`)를 주의 깊게 확인하세요. 슬래시의 유무에 따라 동기화 방식이 달라질 수 있습니다.
- 대량의 파일을 전송할 때는 `-z` 옵션을 사용하여 전송 속도를 개선할 수 있습니다.
- 정기적인 백업을 위해 cron 작업과 함께 rsync를 설정하는 것이 좋습니다.