# DI & Spring Test

## DI

결합도를 낮추고 응집도를 높인다

- Property 주입

- 생성자 주입 (요즘 선호하는 방법)

## Test

V Model

단위 통합 시스템 인수

### Spring Test

#### SpringBootTest

SpringBootTest annotation
	Autowired 사용가능 - 테스트에 필요한 의존성 추가

random 포트 생성 가능
`local.server.port` 로 생성된 포트 확인

random 포트와  restTemplate 을 이용한 테스트는 인수테스트에 가까울 정도로 많은 부담이 든다.

#### MockMvc

MockMvc 를 이용하면 서버를 띄우지 않으면서도 서버를 띄운 것과 마찬가지로 테스트를 해볼 수 있다.

※ 인코딩 문제가 있으면 application.properties 에 속성 추가

MockMvc 를 이용해서 get 을 테스트하면 repository 를 파악하고 있어야 한다.
	하지만 이러면 controller 만 테스트한다는 목적에 부합하지 않는다.
	데이터가 있을 것이라는 "가정"이 너무 많음
	-> spybean 활용

하지만 심지어 이것조차도 버거움

SpringBootTest 는 IoC Container 에 모든 의존성을 추가함
또한 싱크홀 현상이 발생할 수 있음

#### WebMvcTest

WebMvcTest 로 변경해서 테스트하는 객체가 필요한 의존성만 주입시킬 수 있음.

믿을 수 있는 부품을 만듦

MockBean 으로 의존성 주입
