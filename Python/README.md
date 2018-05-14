####  Python Comprehension

Comprehension의 사전적 의미로 '이해', '포함' 이라는 뜻을 가지고 있다.
Python에서는 "한 Sequence가 다른 Sequence (Iterable Object)로부터 (변형되어) 구축될 수 있게한 기능이다" 라는 뜻을 가지나 보다. 이게 무슨말인지 ...
그러니까 한 컬렉션 내에 존재하는 각 요소들을 변형하도록 지원하는 간편한 문법이라고 생각하면 더 쉬울 것 같다.

Python3에서는 아래와 같은 Comprehension이을 갖는다.
- List Comprehension
- Dictionary Comprehension
- Set Comprehension
- Generator Comprehension (Generator Expression)
      
1. List Comprehension
```
[출력표현식 for 요소 in 입력값 [if 조건식]]
```
간단한 예제1) 리스트 안에 존재하는 모든 정수 값을 제곱하여 squares라는 리스트로 출력 하세요.
```
>>> a = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
>>> squares = [x**2 for x in a]
>>> print (squares)
[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```
a라는 리스트를 for루프로 각 요소에 접근하여 제곱하고 squares라는 리스트로 할당했다.

간단한 예제2) 리스트 안에 존재하는 값 중 integer 타입의 값만 추출하여 new라는 리스토로 출력하세요.
```
>>> old = [1, 2, 'A', False, 3]
>>> new = [x for x in old if type(x)==int]
>>> print (new)
[1, 2, 3]
```
if조건을 통해 필터링 할 수 있으며 출력 표현식에 아무 연산을 넣지 않아도 된다.

