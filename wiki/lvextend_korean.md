# [리눅스] Bash lvextend 사용법: 논리 볼륨 크기 확장

## Overview
`lvextend` 명령어는 리눅스에서 논리 볼륨(Logical Volume)의 크기를 확장하는 데 사용됩니다. 이 명령어를 통해 디스크 공간을 효율적으로 관리하고, 필요에 따라 볼륨의 크기를 조정할 수 있습니다.

## Usage
`lvextend` 명령어의 기본 구문은 다음과 같습니다:

```bash
lvextend [options] [arguments]
```

## Common Options
- `-L +size`: 지정한 크기만큼 볼륨을 확장합니다. 예: `-L +10G`는 10GB를 추가합니다.
- `-l +size`: 논리 볼륨의 섹터 수를 기준으로 확장합니다. 예: `-l +100`은 100개의 섹터를 추가합니다.
- `-r`: 파일 시스템을 자동으로 확장합니다. 이 옵션을 사용하면 볼륨을 확장한 후 파일 시스템도 함께 조정됩니다.
- `-n`: 논리 볼륨의 이름을 변경합니다.

## Common Examples
1. **10GB만큼 논리 볼륨 확장하기**
   ```bash
   lvextend -L +10G /dev/vg_name/lv_name
   ```

2. **섹터 수를 기준으로 논리 볼륨 확장하기**
   ```bash
   lvextend -l +100 /dev/vg_name/lv_name
   ```

3. **파일 시스템과 함께 논리 볼륨 확장하기**
   ```bash
   lvextend -r -L +5G /dev/vg_name/lv_name
   ```

4. **특정 크기로 논리 볼륨 크기 설정하기**
   ```bash
   lvextend -L 50G /dev/vg_name/lv_name
   ```

## Tips
- 볼륨을 확장하기 전에 항상 백업을 수행하는 것이 좋습니다.
- `-r` 옵션을 사용하면 파일 시스템을 자동으로 확장할 수 있어 편리합니다.
- 논리 볼륨을 확장한 후, 파일 시스템의 상태를 확인하는 것이 중요합니다. `df -h` 명령어를 사용하여 확인할 수 있습니다.