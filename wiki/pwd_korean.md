# [리눅스] Debian Almquist Shell (dash) pwd 사용법: 현재 작업 디렉토리 출력

## 개요
`pwd` 명령어는 현재 작업 중인 디렉토리의 전체 경로를 출력합니다. 이 명령어는 사용자가 현재 위치한 디렉토리를 확인하는 데 유용합니다.

## 사용법
기본 구문은 다음과 같습니다:

```
pwd [옵션]
```

## 일반 옵션
- `-L`: 심볼릭 링크를 따라 현재 작업 디렉토리를 표시합니다.
- `-P`: 물리적 경로를 따라 현재 작업 디렉토리를 표시합니다.

## 일반 예제
1. 현재 작업 디렉토리 출력:
   ```sh
   pwd
   ```

2. 심볼릭 링크를 따라 현재 디렉토리 출력:
   ```sh
   pwd -L
   ```

3. 물리적 경로를 따라 현재 디렉토리 출력:
   ```sh
   pwd -P
   ```

## 팁
- `pwd` 명령어는 스크립트에서 현재 디렉토리를 확인할 때 유용하게 사용될 수 있습니다.
- 다른 명령어와 함께 사용하여 현재 경로를 기반으로 파일을 찾거나 작업을 수행할 수 있습니다.