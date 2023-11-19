# Hexagonal Architecture

## Solid

### SRP

하나의 변경 사유만이 있어야 한다.

### OCP

확장에 열려있고, 자신의 변경이 다른 곳에 영향을 미치면 안된다.

### LSP

서브타입의 기준은 행위의 관점에서 적용된다.

### ISP

응집력이 없는 인터페이스를 여러 인터페이스로 쪼개야 한다.

### DIP

의존하는 쪽은 의존받는 쪽에게 영향을 미치지 말아야 한다.

## Hexagonal Architecture

비즈니스 로직이 application layer 이외의 layer에서 사용되는 문제를 해결하기 위한 방법

layered architecture와의 차이점은 presentation layer와 data layer의 구분이 없다는 것
