##  Iterator

일단 Iterable객체를(Iterable Object) 라는 것이 있다.
간단하게 말하면 Comprehension이 가능한 List,Set,Dict 라고 보면 될것 같고
좀더 설명 하자면 for문을 써서 하나씩 데이터를 처리 할 수 컬렉션을 Iterable객체 라고 한다.

그런데 컬렉션으로 단정 하는것은 아니고 for문을 써서 데이터를 처리 할 수 있는것이면 
이에 포함되기 때문에 문자열 등(sequence들)도 Iterable 객체라고 부를 수 있다.


-----

1. Iterable 객체의 예

	```
	# 리스트 Iterable 
	for x in [1,2,3]
		print(x)
	# 문자열 Iterable
	for a in "Hello JB"
		print(a)
	```


-----

Iterable 객체들은 내장 함수 Iter()와 함께 사용하게 되며 iterator를 리턴한다.
Iterable 객체에서 실제 iteration을 실행하는 것은 Iterator로서, 
Iterator는 next를 사용하여 다음 요소를 가져오고 만약 다음 요소가 없으면 
StopIteration Exception을 발생시킨다.