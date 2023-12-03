# File Upload

file 업로드를 위해 POST로 api 요청 시에 content-type은 multipart/form-data로 설정해야 함

spring에서 구현하는 방법

- `PostMapping`에 consume 값으로 `'multipart/form-data'` 할당

- DTO로 처리할 경우 기존 `RequestBody`가 아니고 `ModelAttribute`로 처리

test 코드 작성

- 요청 테스트 시에 mockMvc에 기존 `post` 대신 `multipart`로 사용

- 파일 이외의 값을 추가하는 경우, param 사용

서버를 여러 대 두게 되면 파일이 있을 수도 있고 없을 수도 있음

따라서 파일만 따로 외부에 저장하는 작업이 필요

서버의 부하를 줄이기 위해서 별도로 서버리스를 이용해서 파일 업로드를 할 수도 있음
