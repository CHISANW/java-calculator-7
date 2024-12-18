# 1주차 미션 - 문자열 덧셈 계산기

---

## 👩‍💻 구현할 기능 목록

### 목차

- [기능 목록](#기능-목록)
    - [01. 사용자 입력 기능](#01-사용자-입력-기능)
    - [02. 구분자 처리 기능](#02-구분자-처리-기능)
    - [03. 문자열 배열을 List<Integer>으로 반환 기능](#03-문자열-배열을-listinteger으로-반환-기능)
    - [04. 결과 출력 기능](#04-결과-출력-기능)

### 01. 사용자 입력 기능

- 사용자는 문자열을 입력합니다.
- 입력이 `""` (빈 문자열) 이거나 `null`일 경우, 계산 결과는 `0`으로 처리합니다.
- **예시**:
    - 입력: `""`  → 출력: `결과 : 0`
    - 입력: `null` → 출력: `결과 : 0`

### 02. 구분자 처리 기능

- 기본 구분자는 쉼표(,)와 콜론(:)으로 정의합니다.
- 입력된 문자열이 `//`로 시작하는 경우, 커스텀 구분자로 판단합니다. 이 경우 `\n`로 끝나는 문자열까지의 구분자를 기본 구분자로 변경합니다.
- 변경된 구분자를 사용하여 문자열을 배열로 반환합니다.

- **예시**:
    1. 입력: `"1,2,:3"` → 기본 구분자 `[,:]`을 사용하여 반환: `["1", "2", "3"]`
    2. 입력: `"//;\n1;2;3"` → 커스텀 구분자 `[;]`으로 변경 후 반환: `["1", "2", "3"]`

### 03. 문자열 배열을 List<Integer>으로 반환 기능

- 문자열 배열을 통해 각 요소를 숫자로 변환합니다.
- 변환 중 `NumberFormatException`이 발생할 경우, 이를 `IllegalArgumentException`으로 변환하여 예외를 발생시킵니다.

- **예시**:
    1. 입력: `["1", "2", "3"]` → 변환 후: `List<Integer> = [1, 2, 3]`
    2. 입력: `["1", "2", "3a"]` → `3a`는 숫자가 아니므로 `IllegalArgumentException` 발생.

### 04. 결과 출력 기능

- 숫자로 변환된 값을 모두 더하여 합산한 값을 출력합니다.

- **예시**:
    1. `List<Integer> = [1, 2, 3]` → 출력: `결과 : 6`

---

## ✅ 확인할 요구사항 목록

### 기능 요구 사항

- [X] 쉼표(,) 또는 콜론(:)을 구분자로 가지는 문자열을 전달하는 경우 구분자를 기준으로 분리한 각 숫자의 합을 반환한다.
- [X] 앞의 기본 구분자(쉼표, 콜론) 외에 커스텀 구분자를 지정할 수 있다. 커스텀 구분자는 문자열 앞부분의 "//"와 "\n" 사이에 위치하는 문자를 커스텀 구분자로 사용한다
- [X] 사용자가 잘못된 값을 입력할 경우 IllegalArgumentException을 발생시킨 후 애플리케이션은 종료되어야 한다.

### 요구사항

- [X] JDK 21 버전에서 실행 가능해야한다.
- [X] 제공된 라이브러리 이외의 외부 라이브러리는 사용하지 않는다.
- [X] System.exit 메소드를 사용하지 않는다.
- [X] 프로그래밍 요구 사항에서 달리 명시하지 않는 한 파일, 패키지 등의 이름을 바꾸거나 이동하지 않는다
- [X] 자바 코드 컨벤션을 지키면서 프로그래밍한다

### 추가사항

- [X] 각 메서드별 기능 주석 작성
- [X] 각 메서드별 단위 테스트 코드 작성

<br>