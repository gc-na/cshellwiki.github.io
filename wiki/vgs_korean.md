# [리눅스] Bash vgs 사용법: 볼륨 그룹 정보 표시

## Overview
`vgs` 명령어는 리눅스에서 LVM(Logical Volume Manager) 볼륨 그룹의 정보를 표시하는 데 사용됩니다. 이 명령어를 통해 시스템의 볼륨 그룹에 대한 요약 정보를 쉽게 확인할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```
vgs [옵션] [인수]
```

## Common Options
- `-o, --options`: 출력할 필드를 지정합니다.
- `-h, --noheadings`: 헤더를 출력하지 않습니다.
- `-s, --units`: 출력 단위를 설정합니다.
- `--nosuffix`: 단위 접미사를 생략합니다.

## Common Examples
다음은 `vgs` 명령어의 몇 가지 일반적인 사용 예입니다.

1. 기본 볼륨 그룹 정보 표시:
   ```bash
   vgs
   ```

2. 특정 필드만 출력하기 (예: VG 이름과 크기):
   ```bash
   vgs -o vg_name,size
   ```

3. 헤더 없이 정보 출력하기:
   ```bash
   vgs --noheadings
   ```

4. 출력 단위를 MB로 설정하기:
   ```bash
   vgs -s m
   ```

5. 볼륨 그룹의 상세 정보 확인하기:
   ```bash
   vgs -o +pv_count
   ```

## Tips
- `vgs` 명령어는 `lvscan`이나 `pvscan`과 함께 사용하여 LVM의 전체 구조를 이해하는 데 유용합니다.
- 출력 결과를 파일로 저장하고 싶다면 리다이렉션을 사용하여 쉽게 저장할 수 있습니다:
  ```bash
  vgs > vgs_output.txt
  ```
- 자주 사용하는 옵션을 별도의 스크립트로 만들어 두면 효율적으로 작업할 수 있습니다.