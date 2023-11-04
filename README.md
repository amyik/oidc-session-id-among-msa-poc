# oidc-session-id-among-msa-poc

- 서로 다른 sepring security core version을 사용하는 두 서비스간에 redis를 통해 세션 공유가 가능한지 검토
- 두 서비스의 구성
  1. api-gateway : oidc 인증 후 redis에 세션 정보 저장
  2. app-a : redis의 세션 정보를 참조해 비지니스 로직 수행
- 두 서비스는 spring project기반이나 프레임워크의 버전이 달라서 odic인증 결과 세션에 사용하는 객체 타입의 버전이 다르다.( AuthenticationToken )