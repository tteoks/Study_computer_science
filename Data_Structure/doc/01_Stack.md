# Stack의 개념

자료 구조에서 한 쪽 끝에서만 자료를 넣고 빼는 후입선출 특성의 LIFO (Last In First Out) 선형  자료구조

### 주요 연산 

LIFO (Last In First Out) 구조이기 때문에, 가장 최근에 스택에 추가한 항목이 가장 먼저 제거되어야 한다.

* pop 연산: 스택에서 가장 위에 있는 항목을 반환 하며, 제거한다.
* push 연산: 자료를 스택의 가장 윗 부분에 추가한다.
* top 연산: 스택의 가장 위에 있는 항목을 반환한다.
* isEmpty 연산: 스택이 비어있는 경우 true를 반환 / 자료가 존재하는 경우 false를 반환한다.


### Stack 자료구조 특징

* 배열과 달리 스택은 n번째 항목에 직접 접근 할 수 없음
* 스택에서 데이터 추가 및 삭제하는 연산이 다른 자료구조에 비해 빠름
* 배열처럼 원소들을 하나씩 옆으로 밀어줄 수 없음

### Stack의 사용 사례

Stack은 재구 알고리즘을 사용하는 스택이 유용함

* 재귀 알고리즘
  * 재귀적으로 함수를 호출해야 하는 경우 임시 데이터를 스택에 넣어 활용
  * 재귀함수에서 나와 퇴각 검색 (back track)할 때 임시 데이터를 순차적으로 뺴줘야 함
* 웹 브라우저 방문 기록 (뒤로 가기)
* 실행 취소 (Undo)
* 역순 문자열 만들기
* 수식의 괄호 연산 (VPS,Valid Parenthesis String)
* 후위 표기법 계산


출처: https://gmlwjd9405.github.io/2018/08/03/data-structure-stack.html