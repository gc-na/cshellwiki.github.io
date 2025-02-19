# [리눅스] C Shell (csh) getopts 사용법: 옵션을 처리하는 명령

## Overview
`getopts` 명령은 C Shell 스크립트에서 명령줄 옵션을 처리하는 데 사용됩니다. 이 명령은 스크립트가 사용자로부터 입력받은 옵션을 쉽게 파싱하고 처리할 수 있도록 도와줍니다.

## Usage
기본 구문은 다음과 같습니다:

```csh
getopts optstring variable
```

- `optstring`: 허용되는 옵션의 문자열입니다. 각 옵션은 단일 문자로 표현되며, 콜론(:)이 뒤따르면 해당 옵션이 인자를 필요로 함을 나타냅니다.
- `variable`: 옵션의 값을 저장할 변수입니다.

## Common Options
- `-a`: 추가적인 옵션을 지정합니다.
- `-b`: 옵션을 비활성화합니다.
- `-c`: 특정 조건을 설정합니다.

## Common Examples

1. **기본 사용 예제**
   ```csh
   #!/bin/csh
   set optstring = "ab:c"
   while (getopts $optstring option)
       switch ($option)
           case "a":
               echo "옵션 A가 선택되었습니다."
               breaksw
           case "b":
               echo "옵션 B가 선택되었습니다. 인자: $OPTARG"
               breaksw
           case "c":
               echo "옵션 C가 선택되었습니다."
               breaksw
           default:
               echo "유효하지 않은 옵션입니다."
       endsw
   end
   ```

2. **인자를 필요로 하는 옵션 사용**
   ```csh
   #!/bin/csh
   set optstring = "a:b:"
   while (getopts $optstring option)
       switch ($option)
           case "a":
               echo "옵션 A가 선택되었습니다."
               breaksw
           case "b":
               echo "옵션 B가 선택되었습니다. 인자: $OPTARG"
               breaksw
           default:
               echo "유효하지 않은 옵션입니다."
       endsw
   end
   ```

3. **옵션이 없는 경우 처리**
   ```csh
   #!/bin/csh
   set optstring = "a"
   while (getopts $optstring option)
       if ($option == "") then
           echo "옵션이 제공되지 않았습니다."
       endif
   end
   ```

## Tips
- `getopts`는 스크립트에서 옵션을 처리할 때 유용하며, 각 옵션에 대해 적절한 메시지를 출력하여 사용자에게 피드백을 제공하는 것이 좋습니다.
- 인자를 필요로 하는 옵션은 콜론(:)을 사용하여 정의해야 하며, `$OPTARG` 변수를 통해 인자 값을 참조할 수 있습니다.
- 스크립트의 가독성을 높이기 위해 옵션 처리 로직을 깔끔하게 정리하는 것이 중요합니다.