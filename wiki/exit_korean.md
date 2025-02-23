# [리눅스] Debian Almquist Shell (dash) exit 사용법: 셸 종료

## Overview
`exit` 명령은 현재 셸 세션을 종료하는 데 사용됩니다. 이 명령은 스크립트나 인터랙티브 셸에서 실행될 수 있으며, 종료 코드(상태)를 지정할 수 있습니다.

## Usage
기본 구문은 다음과 같습니다:
```
exit [options] [arguments]
```

## Common Options
- `n`: 종료 코드로 사용할 숫자를 지정합니다. 기본적으로 0은 성공, 1은 실패를 나타냅니다.

## Common Examples
- 기본적으로 셸 종료:
  ```sh
  exit
  ```

- 특정 종료 코드로 셸 종료:
  ```sh
  exit 1
  ```

- 스크립트에서 사용하여 종료 코드 반환:
  ```sh
  #!/bin/dash
  echo "스크립트가 종료됩니다."
  exit 0
  ```

## Tips
- 스크립트에서 `exit` 명령을 사용할 때, 적절한 종료 코드를 반환하여 후속 프로세스가 결과를 이해할 수 있도록 하세요.
- 인터랙티브 셸에서 `exit`를 입력하면 현재 세션이 종료되므로, 중요한 작업이 완료된 후에 사용하는 것이 좋습니다.