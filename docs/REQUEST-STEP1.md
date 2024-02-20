# 로또 애플리케이션 기능 요구 사항

어느 평화로운 개발팀,
개발하다 한번씩 심심풀이로 돌려보는 용도로 간단한 콘솔 기반의 로또 게임을 만들어 보기로 한다.

## 로또

- 사용자가 구매한 로또 번호와 당첨 번호를 비교한다.
- 보너스 번호를 포함하는지 비교한다.
- 로또는 1 ~ 45의 6개의 숫자로 구성되어있다.
  - 숫자가 아닌 문자열이 들어오면 안된다.
  - 6개의 숫자로 구성되어야 한다.
  - 1 ~ 45 사이의 숫자여야 한다.
  - 로또는 중복된 숫자를 가질 수 없다

## 로또 상점

- 로또 구입 금액을 입력하면 구입 금액에 해당하는 만큼 로또를 발행해야 한다.
  - 로또 번호는 중복이 없는 1~45사이의 랜덤 숫자 배열이다.
- 로또 1장의 가격은 1,000원이다.
  - 로또 가격은 문자열(공백)이 될 수 없다.
  - 로또 가격은 1,000으로 나누어떨어져야 한다.

## 로또 결과

- 로또 결과판을 만든다.
  - 등수와 각 등수의 갯수 정보로 구성되어있다.
- 수익률을 계산한다.
  - 수익률은 `총 당첨금/구입 금액`이다.
- 당첨은 1등부터 5등까지 있다. 당첨 기준과 금액은 아래와 같다.

```text
1등: 6개 번호 일치 /
0원
2등: 5개 번호 + 보너스 번호 일치 / 30,000,000원
3등: 5개 번호 일치 / 1,500,000원
4등: 4개 번호 일치 / 50,000원
5등: 3개 번호 일치 / 5,000원
```

## 입력

- 당첨 번호와 보너스 번호를 입력받는다.
- 당첨 통계를 출력한 뒤에는 재시작/종료 여부를 입력받는다.

## 출력

- 로또 번호는 오름차순으로 정렬하여 보여준다.
- 당첨 내역 및 수익률을 출력한다.

## 기타

- 사용자가 잘못된 값을 입력한 경우 throw문을 사용해 예외를 발생시키고, 에러 메시지를 출력 후 그 부분부터 입력을 다시 받는다.
- 재시작할 경우 구입 금액 입력부터 게임을 다시 시작하고, 종료하는 경우 그대로 프로그램을 종료시킨다.