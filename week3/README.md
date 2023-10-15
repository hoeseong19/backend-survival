# DTO, JSON, Serialize, Jackson Object Mapper, CORS

## Jackson Object Mapper

PathVariable, RequestBody 상관하지 않고 모두 Dto로 변환해준다.

Response 에서 jackson 을 이용하려면 모든 필드의 getter 가 존재해야 된다

아니면 406 에러남,,,

## Cors

### Same-Origin Policy

Http 통신에서 요청과 응답의 **출처**가 같아야 하는 정책

그래서 localhost:3000과 localhost:8080이 통신하면 호스트가 다르기 때문에 정책에 부합하지 않아서 서버의 응답이 잘 됐음에도 불구하고 에러가 남

### 해결 방법

#### Jsonp

&lt;script&gt;안에서는 same origin policy 가 적용되지 않음. 그래서 서버에서 자바스크립트 코드를 반환하는 걸로 해결했었음

~~요즘은 사용안함~~

#### Cross-Origin Resource Sharing

Same origin policy 는 브라우저가 발생시키는 에러

서버에서 브라우저한테 특정 origin 은 괜찮다고 알려준 origin 은 에러를 발생시키지 않는 방법

##### Spring Web Mvc 에서 사용하는 방법

- response header에 명시적으로 `Access-Control-Allow-Origin` 추가

- CrossOrigin 데코레이터 사용클래스와 메서드 둘 다 붙일 수 있음

    - 만약 매개변수가 없다면 와일드 카드

- WebMvcConfigurer를 사용해서 서버 전체에 적용시키는 방법
