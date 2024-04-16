# Chapter 4. 아키텍처

## 4.1 MySQL 엔진 아키텍처
* MySQL은 MySQL 엔진과 스토리지 엔진으로 구성된다.
  1. MySQL 엔진
     - 커넥션 핸들러 : 쿼리 요청을 처리
     - SQL 파서
     - 전처리기
     - 옵티마이저
  2. 스토리지 엔진
      - 실제 데이터를 디스크에 저장하고 읽어오는 부분을 담당한다.
      - 플러그인으로 다양한 기능을 제공한다. -> 컴포넌트로 변경됨
      - InnoDB, MyISAM, Memory, CSV, Archive 등이 있다.

    
* 핸들러 API : MySQL 엔진과 스토리지 엔진 사이의 인터페이스
  - SHOW GLOBAL STATUS LIKE 'Handler%'; 명령어로 확인 가능


