# 프리코스 2주차 미션 - 자동차 경주
![우아한테크코스](https://github.com/user-attachments/assets/f877bb9f-faf7-4b27-8344-686b5337a962)

![Generic badge](https://img.shields.io/badge/precourse-week2-green.svg)
![Generic badge](https://img.shields.io/badge/version-1.0.1-brightgreen.svg)
![Generic badge](https://img.shields.io/badge/test-0_passed-blue.svg)

## 목차
- [요구사항](#-요구사항)
    - [기능 요구사항](#기능-요구사항)
    - [입출력 요구사항](#입출력-요구사항)
- [기능 목록](#-기능-목록)
    - [입력](#-입력)
    - [경주](#-경주)
    - [자동차 동작](#-자동차의-동작)
    - [출력](#-출력)

<br>

## 🚀 요구사항

### ✔️ 기능 요구사항

+ 주어진 횟수 동안 n대의 자동차는 전진 또는 멈출 수 있다.
+ 각 자동차에 이름을 부여할 수 있다. 전진하는 자동차를 출력할 때 자동차 이름을 같이 출력한다.
+ 자동차 이름은 쉼표(,)를 기준으로 구분하며 이름은 5자 이하만 가능하다.
+ 사용자는 몇 번의 이동을 할 것인지를 입력할 수 있어야 한다.
+ 전진하는 조건은 0에서 9 사이에서 무작위 값을 구한 후 무작위 값이 4 이상일 경우이다.
+ 자동차 경주 게임을 완료한 후 누가 우승했는지를 알려준다. 우승자는 한 명 이상일 수 있다.
+ 우승자가 여러 명일 경우 쉼표(,)를 이용하여 구분한다.
+ 사용자가 잘못된 값을 입력할 경우 `IllegalArgumentException`을 발생시킨 후 애플리케이션은 종료되어야 한다.

<br>

### ✔️ 입출력 요구사항

+ 입력
  + 경주할 자동차 이름(이름은 쉼표(,) 기준으로 구분)
    ```
    pobi,woni,jun
    ```
  + 시도할 횟수
    ```
    5
    ```
+ 출력
  + 차수별 실행결과
    ```
     결과 : 6
    ```
  + 단독 우승자 안내 문구
    ```
    최종 우승자 : pobi
    ```
  + 공동 우승자 안내 문구
    ```
    최종 우승자 : pobi, jun
    ```
+ 실행결과 예시
  ```
  경주할 자동차 이름을 입력하세요.(이름은 쉼표(,) 기준으로 구분)
  pobi,woni,jun
  시도할 횟수는 몇 회인가요?
  5

  실행 결과
  pobi : -
  woni :
  jun : -

  pobi : --
  woni : -
  jun : --

  pobi : ---
  woni : --
  jun : ---

  pobi : ----
  woni : ---
  jun : ----

  pobi : -----
  woni : ----
  jun : -----

  최종 우승자 : pobi, jun
  ```

<br>

## 🎯 기능 목록

### ✔️ 입력

- [ ] 자동차의 이름을 입력한다.
  - [ ] 자동차의 이름은 쉼표(,)를 기준으로 구분한다.
  - [ ] `추가적인 예외처리` : 입력받는 자동차의 개수는 10000이하로 제한한다.
  
- [ ] 몇 번의 이동을 할 것인지 입력한다.
  - [ ] `예외처리` : 공백일 경우 `IllegalArgumentException`
  - [ ] `예외처리` : 숫자가 아닐 경우 `IllegalArgumentException`
  - [ ] `추가적인 예외처리` : 입력받는 숫자는 10000이하로 제한한다. 

<br>

### ✔️ 경주
- [x] 주어진 횟수 동안 N대의 자동차는 전진 또는 멈출 수 있다.
- [ ] 가장 멀리 위치한 자동차를 알 수 있다.

<br>

### ✔️ 자동차의 동작
- [x] 자동차는 전진 또는 멈춤을 할 수 있다.
  - [x] 전진일 경우 한 칸 앞으로 나간다.
  - [x] 멈춤일 경우 가만히 있는다.
- [x] 자동차는 [0, 9] 사이의 무작위 값에서 4 이상이 나왔을 경우 전진한다. 
  - [ ] `예외처리` : 0 미만, 9 초과의 값이 나올 경우 `IllegalArgumentException`
- [x] 자동차는 [0, 9] 사이의 무작위 값에서 4 미만이 나왔을 경우 멈춘다. 
  - [ ] `예외처리` : 0 미만, 9 초과의 값이 나올 경우 `IllegalArgumentException`
- [x] 자동차의 이름은 5자 이하만 가능하다.
  - [x] 자동차의 이름에서 공백이 포함될 경우, 공백 제외 5자 이하만 가능하다.
  - [x] `예외처리` : 빈 문자열일 경우 `IllegalArgumentException`
  - [x] `예외처리` : 5자 이상일 경우 `IllegalArgumentException`
<br>


### ✔️ 출력
- [ ] `실행 결과` 를 출력한다.
- [ ] 경주가 한 번 진행될 때마다 결과를 출력한다.
  - [ ] N대의 자동차를 `자동차의 이름` : `진행 거리` 로 나타내어 출력한다.
  - [ ] 모든 자동차를 출력한 후 개행한다.
- [ ] 최종 우승자를 출력한다.
  - [ ] 우승자는 1명 이상일 수 있다.
  - [ ] 우승자가 여러 명일 경우, 쉼표(,)을 통해 우승자의 이름을 구분하여 출력한다.

