# [리눅스] Debian Almquist Shell (dash) free 메모리 사용량 확인: 시스템 메모리 상태를 보여줍니다.

## Overview
`free` 명령은 시스템의 메모리 사용량을 확인하는 데 사용됩니다. 이 명령은 사용 중인 메모리, 사용 가능한 메모리, 스왑 메모리 등의 정보를 제공합니다. 시스템의 메모리 상태를 모니터링하고 성능을 최적화하는 데 유용합니다.

## Usage
기본 구문은 다음과 같습니다:

```bash
free [options]
```

## Common Options
- `-h`: 사람이 읽기 쉬운 형식으로 메모리 정보를 표시합니다.
- `-m`: 메모리 정보를 메가바이트 단위로 표시합니다.
- `-g`: 메모리 정보를 기가바이트 단위로 표시합니다.
- `-s <seconds>`: 지정한 초 간격으로 메모리 정보를 반복해서 표시합니다.
- `-t`: 총 메모리 사용량을 포함하여 표시합니다.

## Common Examples
다음은 `free` 명령의 몇 가지 유용한 예입니다:

1. 기본 메모리 정보 확인하기:
   ```bash
   free
   ```

2. 사람이 읽기 쉬운 형식으로 메모리 정보 확인하기:
   ```bash
   free -h
   ```

3. 메가바이트 단위로 메모리 정보 확인하기:
   ```bash
   free -m
   ```

4. 5초 간격으로 메모리 정보 반복해서 확인하기:
   ```bash
   free -s 5
   ```

5. 총 메모리 사용량 포함하여 확인하기:
   ```bash
   free -t
   ```

## Tips
- `free -h` 옵션을 사용하면 메모리 정보를 쉽게 이해할 수 있습니다.
- 시스템의 메모리 사용량을 정기적으로 모니터링하여 성능 문제를 조기에 발견할 수 있습니다.
- `watch` 명령과 함께 사용하여 실시간으로 메모리 사용량을 모니터링할 수 있습니다. 예를 들어:
  ```bash
  watch free -h
  ```