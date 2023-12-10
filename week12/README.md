# CQRS

CUD: Command
R: Query

둘을 분리하고 싶다. 

메서드 단위의 SRP가 적용되는 것이로 인해 side effect가 줄어 듦

둘을 분리하기 위해서 db를 나눌 수도 있음

동기화는 event sourcing으로 처리한다. 

Materialized View: View를 주기적으로 동기화하여 성능을 향상킨다
