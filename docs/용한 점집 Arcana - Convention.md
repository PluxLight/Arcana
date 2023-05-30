# Convention

## Git Commit Convention

- 구조

  - 기본적으로 커밋 메시지는 아래와 같이 제목/본문/꼬리말로 구성

    ```
    type : subject

    body

    footer
    ```

  - 커밋 타입(Type)
    - feat : 새로운 기능 추가
    - add : 기존에 있던 내용 중 기능을 더 추가
    - fix : 버그 수정
    - del : 기존 내용 삭제
    - docs: 문서 내용 변경
    - style: 포맷, 세미콜론 수정 등 코드가 아닌 스타일에 관련된 수정
    - refactor: 리팩토링 코드
    - test: 테스트 코드 추가 및 리팩토링 테스트 등
    - chore: build task 수정, 프로젝트 매니저 설정 수정 등
    - 타입은 소문자로 시작
    - 타입은 항상 대괄호 안에 파트를 입력하여 시작
    - 예시
      - "fix" --> ''[HW] fix'
  - 제목(Subject)
    - 제목은 50자 이내로, 대문자로 시작하며 모두 소문자로 작성
    - 파일명의 경우에는 대소문자 고려하지 않음
    - 마침표로 끝나지 않도록 함
    - 과거시제를 사용하지 않고 명령어로 작성
    - 예시
      - "feat : Logined" --> "feat : Login"
      - "feat : Added" --> "feat : Add"
  - 본문(Body)
    - 선택사항
    - 부연 설명 필요 시 작성
    - 100자 미만 작성 권장
  - 꼬리말(Footer)
    - 선택사항
    - issue tracker id를 작성할 때 사용
    - JIRA Code 작성 시 사용
  - 예시

    ```
    feat : 로그인

    한글한글한글
    - 영어말고 한글로
    - 선택사항
    ```

<br>

## Git Branch Convention

### Branch

- master
  - 배포 가능한 상태의 결과물
- develop
  - 구현한 기능을 병합하기 위한 브랜치
  - 통합 폴더의 기능
  - fe, be로 구분
  - 네이밍 규칙
  - 슬래시 `/` 로 구분
  - dev/파트/기능
  - 예)

    - dev-fe 해당 브랜치에서 작성할시
    - dev-fe/ [작업중인 페이지]
    - 커밋은 최대한 자주 해주세요
    - 커밋시 문구는 위에 적혀 있습니다.
    - ex) 내가 mainPage에서 로그인 기능을 최초로 만들었다 했을때
      1. dev-fe브랜치에서 mainPage브랜치 생성
      2. 작업 완료후 커밋시 feat: 로그인 기능
      - dev-be

    ### Merge 관련

    - MR은 Git lab을 통해 요청 및 수락
    - 공통 개발 브랜치 본인 브랜치에 먼저 pull해서 충돌 여부 확인할 것
    - 비밀 Merge 금지
      - 최소한 FE는 FE끼리, BE는 BE끼리 공유하기
    - MR시
      - title : merge하려는 브랜치 이름
      - description : 비우기
      - 머지 후 브랜치 삭제
      - 어느 브런치로 Merge 하는지 대괄호안에 명시
        - ex) feat/fe/login → feat/fe로 머지할 때.
        - [fe]

## Jira Convention

매일 옮겨놓기

에픽 생성시 ‘FE 중분류’ / ‘BE 중분류’ 형태로 해놓기

말머리를 생성하지 않고 FE, BE 에픽을 상세히 만들기

## Code Convention

- Front
  - Typescript
  - airbnb 스타일 ESLint
    ```jsx
    // 이름 지정 : React 구성 요소에는 PascalCase를 사용
    // 해당 인스턴스에는 camelCase를 사용

    // bad
    import reservationCard from "./ReservationCard";

    // good
    import ReservationCard from "./ReservationCard";

    // bad
    const ReservationItem = <ReservationCard />;

    // good
    const reservationItem = <ReservationCard />;
    ```
  - styled component
  - state 관리자 ⇒ **Zustand!!**
  - node.js v18.16.0
  - 라이브러리
    - 설치시 꼭 꼭 말은 하기
- Back
  - Google Code Style
  - [Google Java Guide 원문](https://google.github.io/styleguide/javaguide.html#s5.3-camel-case)
  - [Google Java Guide 번역](https://newwisdom.tistory.com/96)
  - [Code Style XML GitHub](https://github.com/google/styleguide)
  - [Intellij에 Google Code Style 적용하기](https://tychejin.tistory.com/334)
