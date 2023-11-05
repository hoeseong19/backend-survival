# JPA

## Orm

객체와 데이터를 연결해주는 도구 혹은 방법

sql과 관련된 작업을 자동으로 처리해 줘서 비지니스 로직에 집중할 수 있고, 여러 RDBMS에 종속받지 않는다.

Jakarta EE

기존 JAVA EE에서 오픈소스의 성격을 드러내기 위해 이름이 바뀌었다. 

## JPA

Hibernate vs eclipseLink

이전부터 써오던 방식 vs 공식적인 참조 구현

## JPA Entity

DB vs OOP

## Hibernate

EntityManager & Factory

연결정보는 xml 파일에 기입해야 한다.

@Entity로 DB entity와 OOP entity의 연관관계를 명시

@Table로 name 속성을 이용하여 db의 테이블 이름 지정
@Column으로 name 속성을 이용하여 column 이름 지정

@Id 가 없으면 에러 발생
매개변수가 없는 생성자가 없으면 에러 발생

조회(select)가 아닌 명령(insert, update, delete)은 트랜잭션이 필요하다

PersistenceContext로 인해 객체의 데이터를 바꿔줘도 db에 적용됨

## Embeddable

Entity vs VO

Entity: 식별자가 있고 상태가 변하는 것

primitive type 대신 value object 를 사용해서 속성에 책임들을 위임함으로써 단일책임원칙을 따를 수 있다.

## Relational mapping 

Entity 소유 관계를 정의하는 방법

one to many 관계에서 one에 many의 리스트를 속성으로 정의하면 됨

나중에 ddd lite 할 때 aggregate 라는 이름으로 다시 다룰 예정

## Spring Data Api

모든 걸 쉽게 바꿔 주는 Spring Data Api

`@Transactional`을 테스트에서 쓰면 실행 후에 rollback이 이루어짐
