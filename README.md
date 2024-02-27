# kotlin-lotto

## 기능 요구 사항

- 로또 구입 금액을 입력하면 구입 금액에 해당하는 로또를 발급해야 한다.
- 로또 1장의 가격은 1000원이다.

## 기능 명세

### 뷰
#### 입력
- [x] 구매 금액을 입력받는다.
- [x] 수동으로 구매할 로또의 수를 입력받는다.
- [x] 수동으로 구매할 로또의 수만큼 로또 번호를 입력한다.
- [x] 당첨 번호를 입력받는다.
- [x] 보너스 번호를 입력받는다.
#### 출력
- [x] 수동/자동으로 구매한 로또의 수를 표출한다.
- [x] 구매한 로또들의 리스트를 보여준다.
- [x] 당첨 통계를 보여준다.
  - [x] 당첨 결과를 보여준다.
  - [x] 수익률을 보여준다.

### 컨트롤러
- [x] 수익률 소수점 이하 2자리수까지 버림
- [x] RankResults 에서 Missing 필터링
- [x] 보너스 번호가 당첨 번호 중에 하나 일 때 예외 발생 
- [x] IllegalArgumentException, IllegalStateException 발생 시 재 입력 받기

### 도메인
- [x] 로또 숫자는 1 ~ 45이다.
- [x] 가격을 설정 할 수 있다.
- [x] 로또는 한 장 당 1000원이다.
- [x] 금액에 해당하는 개수만큼 로또를 발급한다.
- [x] 로또는 한 장 당 6개의 숫자를 가지고 있다.
- [x] 로또 한 장에 들어있는 숫자는 중복될 수 없다.
- [x] 로또 숫자들은 오름차순으로 정렬되어야 한다.
- [x] 발행된 한 장의 로또와 당첨 로또와 비교한다.(Lotto 객체에서)
- [x] 로또가 보너스 번호를 가지고 있는지 비교한다.(Lotto 객체에서)
- [x] 당첨 + 보너스 번호와 로또의 숫자들을 비교하여 당첨 순위를 결정한다. (Rank)
- [x] 당첨 순위 별 로또 개수를 산출한다. 
- [x] 수익률을 계산하고, 손익 여부를 판단한다.
- [x] 로또의 개수는 음수가 될 수 없다.

## 질문 목록
- RandomLottoGenerator 에서 price 를 생성자에서 받을 것인가, generate() 파라미터로 받을 것인가??
(저희는 lotto 가격을 결정하는 주체가 RandomLottoGenerator 라고 생각하기 때문에 생성자에 위치했습니다.)
