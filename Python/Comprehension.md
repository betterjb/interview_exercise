##  Python Comprehension

Comprehension의 사전적 의미로 '이해', '포함' 이라는 뜻을 가지고 있다.
Python에서는 "한 Sequence가 다른 Sequence (Iterable Object)로부터 (변형되어) 구축될 수 있게한 기능이다" 라는 뜻을 가지나 보다. 이게 무슨말인지 ...
그러니까 한 컬렉션 내에 존재하는 각 요소들을 변형하도록 지원하는 간편한 문법이라고 생각하면 더 쉬울 것 같다.

Python3에서는 아래와 같은 Comprehension이을 갖는다.
- List Comprehension
- Dictionary Comprehension
- Set Comprehension
- Generator Comprehension (Generator Expression)


-----

1. List Comprehension

	```
	[출력표현식 for 요소 in 입력값 [if 조건식]]
	```
	>간단한 예제1) 리스트 안에 존재하는 모든 정수 값을 제곱하여 squares라는 리스트로 출력 하세요.
	```
	>>> a = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
	>>> squares = [x**2 for x in a]
	>>> print (squares)
	[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
	```
	a라는 리스트를 for루프로 각 요소에 접근하여 제곱하고 squares라는 리스트로 할당했다.

	>간단한 예제2) 리스트 안에 존재하는 값 중 integer 타입의 값만 추출하여 new라는 리스토로 출력하세요.
	```
	>>> old = [1, 2, 'A', False, 3]
	>>> new = [x for x in old if type(x)==int]
	>>> print (new)
	[1, 2, 3]
	```
	if조건을 통해 필터링 할 수 있으며 출력 표현식에 아무 연산을 넣지 않아도 된다.

-----

2. Dictionary Comprehension

	```
	{Key:Value for 요소 in 입력값 [if 조건식]}
	```
	>간단한 예제1) Dict내에 key와 value를 {value:key}와 같은 형태로 변경하세요.
	```
	>>> name_dict = {1:'JB', 2:'Tom', 3:'John'}
	>>> id_dict = {val:key for key,val in name_dict.items()}
	>>> print(id_dict)
	{'John': 3, 'JB': 1, 'Tom': 2}
	```
	>간단한 예제2)  if 조건식 안에 필터링 함수를 사용한 경우입니다. 1부터 50까지 홀수를 Dictionary key로 하고, 그 홀수의 제곱을 value로 할당하는 dict를 객체를 생성하세요.
	```
	>>> def isodd(val):
	...     return val % 2 == 1
	...
	>>> dict_ex = {x:x**2 for x in range(51) if isodd(x)}
	>>> print (dict_ex)
	{1: 1, 3: 9, 5: 25, 7: 49, 9: 81, 11: 121, 13: 169, 15: 225, 17: 289, 19: 361, 21: 441, 23: 529, 25: 625, 27: 729, 29: 841, 31: 961, 33: 1089, 35: 1225, 37: 1369, 39: 1521, 41: 1681, 43: 1849, 45: 2025, 47: 2209, 49: 2401}
	```
	
-----

3. Set Comprehension
	List 를 Dict 형태로 리턴시키는데 이때 {key:value} 형태가 아니고, {...} 형태로 리턴되기 때문에 완벽한 Dict라고 보기는 어렵다.
