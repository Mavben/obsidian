# JPA에서 데이터를 조회하는 방식


- JPA에서 데이터를 조회할 때 `즉시 로딩(EAGER)과 지연 로딩(LAZY)` 두 가지 방식이 있다. 
- 실무에서 가급적이면 ==지연로딩==을 사용해야 한다.
	- 이유는?
	- 즉시 로딩에서는 만약 연관된 데이터를 조회하는 쿼리가 1000개가 된다면 1개의 쿼리를 날리더라도 SQL 쿼리가 추가로 1000개가 나가게 된다.
- Fetch의 디폴트 값
	- @xxToOne : EAGER
	- @xxToMany : LAZY


# FetchType.EAGER

- 즉시 로딩 방식
- 데이터를 조회할 때 연관된 데이터까지 한 번에 불러오는 것

# FetchType.LAZY

- 지연 로딩 방식
- 필요한 시점에 연관된 데이터를 불러오는 것




