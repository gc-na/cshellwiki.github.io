# [리눅스] Bash chgrp 사용법: 파일 그룹 변경

## Overview
`chgrp` 명령어는 파일이나 디렉토리의 소유 그룹을 변경하는 데 사용됩니다. 이 명령어를 통해 특정 파일이나 디렉토리에 대한 접근 권한을 관리할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```
chgrp [옵션] [그룹] [파일/디렉토리]
```

## Common Options
- `-R`: 재귀적으로 하위 디렉토리와 파일의 그룹을 변경합니다.
- `-v`: 변경된 내용을 자세히 출력합니다.
- `-c`: 변경된 파일에 대한 정보를 출력합니다.

## Common Examples
1. 특정 파일의 그룹 변경:
   ```bash
   chgrp developers myfile.txt
   ```

2. 여러 파일의 그룹 변경:
   ```bash
   chgrp developers file1.txt file2.txt file3.txt
   ```

3. 디렉토리의 그룹을 재귀적으로 변경:
   ```bash
   chgrp -R developers mydirectory/
   ```

4. 변경 사항을 자세히 출력:
   ```bash
   chgrp -v developers myfile.txt
   ```

5. 변경된 파일에 대한 정보 출력:
   ```bash
   chgrp -c developers myfile.txt
   ```

## Tips
- 그룹 변경 시, 현재 사용자의 권한이 필요합니다. 사용자가 해당 그룹의 멤버여야 합니다.
- `chgrp` 명령어를 사용할 때는 신중하게 그룹을 설정해야 하며, 잘못된 그룹 변경은 파일 접근에 영향을 줄 수 있습니다.
- `ls -l` 명령어를 사용하여 파일의 현재 그룹을 확인한 후 변경하는 것이 좋습니다.