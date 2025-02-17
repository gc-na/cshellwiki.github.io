# [리눅스] Bash unset 사용법: 변수 삭제

## Overview
`unset` 명령어는 Bash에서 변수나 함수의 값을 삭제하는 데 사용됩니다. 이 명령어를 사용하면 특정 변수나 함수가 더 이상 존재하지 않도록 할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
unset [options] [arguments]
```

## Common Options
- `-f`: 함수 삭제를 지정합니다.
- `-v`: 변수를 삭제할 때 사용합니다. 기본적으로 이 옵션은 필요하지 않지만 명시적으로 사용할 수 있습니다.

## Common Examples

1. **변수 삭제**
   ```bash
   my_var="Hello, World!"
   echo $my_var  # 출력: Hello, World!
   unset my_var
   echo $my_var  # 출력: (빈 값)
   ```

2. **함수 삭제**
   ```bash
   my_function() {
       echo "This is a function"
   }
   my_function  # 출력: This is a function
   unset -f my_function
   my_function  # 오류: my_function: command not found
   ```

3. **여러 변수 한 번에 삭제**
   ```bash
   var1="First"
   var2="Second"
   unset var1 var2
   echo $var1  # 출력: (빈 값)
   echo $var2  # 출력: (빈 값)
   ```

## Tips
- `unset` 명령어를 사용할 때 주의해야 할 점은, 삭제된 변수나 함수는 복구할 수 없으므로 신중하게 사용해야 합니다.
- 스크립트에서 불필요한 변수를 정리할 때 유용하게 사용할 수 있습니다.
- 변수를 삭제한 후에는 해당 변수가 존재하지 않음을 확인하는 것이 좋습니다.