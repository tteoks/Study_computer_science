# 다양한 알고리즘 (Miscellaneous Algorithm)

알아 두면 도움이 될 수 있는 다양한 알고리즘  

Miscellaneous Algorithms  
* 파보나치 수 (Fibonacci numbers)
* 유클리드 호제법 (Euclidean algorithm)
* 파스칼의 삼각형 (Pascal's triangle)
* 행렬 곱셈 (Matrix multiplication)
* Maximum subarray algorithm

## 파보나치 수 (Fibonacci numbers)

파보나치 수열은 이전 두 항을 더하여 다음 항을 만들어내는 수열이다.

파보나치 수열 공식
> 1. F(0) = 0, F(1) = 1
> 2. F(n) = F(n - 1) + F(n - 2)


파보나치 수열은 수학적 공식으로 나타내지만, 자연계 많은 곳에서 실제로 발견되는 등 아름다운 수열로 불리운다.

그래프로 나타내면, 소라의 나선모양, 꽃잎의 배열 등의 나선 모양으로 나타난다.
해당 수열은 컴퓨터 과학이나 알고리즘에서도 종종 사용된다.

파보나치 수열의 특징
* 규칙성: 각 항이 이전 두 항의 합으로 정의되는 규칙적 수열
* 지수적 증가: n이 증가함에 따라 F(n)의 값이 기하급수적으로 증가
* 근사적 비율: 연속하는 항들의 비율이 황금비율로 수렴 (약 1.618)
* 파보나치 비율: 파보나치 수열에서 각 항을 이전항으로 나눈 비율을 파보나치 비율이라하며, 이 비율을 황금비율과 동일함


## 유클리드 호제법 (Euclidean algorithm)
유클리드 호제법은 2개의 자연수 또는 다항식의 최대 공약수 (GCD: Greatest Common Divisor)를 구하는 효율적인 알고리즘이다.
* 호제법: 두 수가 서로 상대방 수를 나누어서 결국 원하는 수를 얻는 알고리즘


유클리드 호제법 원리
> 두 양의 정수 a, b (a > b)에 대하여 a = bq + r (0 <= r < b)인 경우, a, b의 최대공약수는 b, r의 최대공약수와 같다  
> 즉, gcd(a, b) = gcd(b, r)  
> r = 0 이라면, a, b의 최대공약수는 b가 된다.


두 정수 A, B의 최대 공약수를 구하는 과정 (A > B)
1. A를 B로 나눈 나머지 R을 계산
2. R이 0인 경우, B가 최대 공약수이다. 즉, gcd(A, B) = B
3. R이 0이 아닌 경우, 1번에서 A에 B, B에 R을 넣고 2번 진행

알고리즘 동작 예시  
(1071, 1029) = (1029, 42) = (42, 21) = (21, 0) = 21

## 파스칼의 삼각형 (Pascal's triangle)
수학에서 이항계수를 삼각형 모양의 기하학적 형태로 배열할 것이다.
* 이항계수: 서로 다른 몇 개의 물건 중에서 순서없이 물건을 선택할 수 있는 경우의 수
* 블레즈 파스칼에 의해 명명되었지만, 이미 수세기전부터 연구 된 것

파스칼 삼각형 공식
* 삼각형 맨 위에는 1을 가짐
* 각 행의 양 끝에 1을 가짐
* 그 외 각 숫자는 바로 위 행의 대각선 사으이 두 숫자를 더한 값

파스칼 삼각형은 다양한 수학적, 통계학적 성질을 가짐
* 각 행의 합은 2의 거듭 제곱으로 나타낼 수 있음
* 이항정리에서 계수들의 값을 계산하는데 사용될 수 있음
* 그 외 다양한 수학적 성질을 가지고 있음



## 행렬 곱셈 (Matrix multiplication)
행렬 곱셈은 두 개의 행렬에서 한 개의 행렬을 만들어내는 이항연산이다.
* 단, 첫번째 행렬의 열 개수와 두 번째 행렬의 행 개수가 동일해야 함
* 게산된 행렬은 첫번째 행렬의 행 개수와, 두번째 행렬의 열 개수를 가진다.
* 행렬 A와 B의 곱은 간단히 AB로 나타냄
* m x n 행렬과 n x k 행렬의 곱은 m x k 행렬이 된다.

행렬 곱셈 공식
* 첫번째 행렬의 행(row)와 두번째 행렬의 열(column)의 각 요소들을 곱함
* 위에서 곱한 값들을 모두 더하여 새로운 행렬에 값을 삽입
(그림이 필요할 듯)

행렬 곱셈의 특징
* 행렬 곱셈은 교환 법칙이 성립하지 않음
  * A * B와 B * A가 같지 않을 수 있음
* 행렬 곱셈은 결합 법칙이 성립됨
  * (A * B) * C = A * (B * C) 임


## Maximum subarray problem
최대 부분 배열 문제는 주어진 배열에서 연속된 부분 배열 (Subarray) 중에서 원소의 합이 최대가 되는 부분 배열을 찾는 문제이다.

예시  
[1, -5, 3, 6, -2] 배열에서는 [3, 6] 부분 배열이 원소 합이 9이므로, 해당 배열의 Maximum subarray는 [3, 6]이 된다.

해당 문제를 풀기 위한 다양한 접근법
1. 완전 탐색 (Brute force)
2. 동적 프로그래밍 (Dynamic Programming)
3. Kadane's 알고리즘

