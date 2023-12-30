# Optional

```java
List<Integer> someNumbers = Arrays.asList(1, 2, 3, 4, 5);
Optional<Integer> firstSquareDivisibleByThree = 
	someNumbers.stream()
				.map(n -> n * n)
				.filter(n -> n % 3 == 0)
				.findFirst(); // 9
```

- Optional<T> 클래스 - 값의 존재나 부재 여부 표현하는 컨테이너 클래스
- null은 쉽게 에러를 일으킬 수 있으므로 자바 8 라이브러리 설계자는 Optional<T>를 만들었다.
- 리스트 또는 정렬된 연속 데이터로부터 생성된 스트림은 논리적인 아이템 순서가 정해져 있을 수 있다.
