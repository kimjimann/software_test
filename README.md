# 구글은 소프트웨어를 어떻게 테스트하는가

1장 구글 소프트웨어 테스팅 개요

- 생산성 혁신팀의 주 업무
  1. 개발자와 테스터의 툴 체인 수행
  2. 단위 테스팅부터 탐색적 테스팅과 관련된 공학적 방법 적용
  3. 모든 웹 특성과 관련된 공용 툴과 테스트 인프라스트럭처 구축

- 소형 테스트 (코드가 제대로 작동하는가)
  1. 적은 양의 코드를 test, 실무에서는 대부분 자동화 테스트로 수행되며 단일함수 or 모듈의 코드를 test한다. (mock, fake 개채 필요)
  
  
- 중형 테스트 (상호작용이 잘되고 있는가)
  1. 일반적으로 자동화 테스트로 수행되며 두번 이상의 인터랙션 기능을 포함한다.
  2. 기능간 상호작용 or 상호 호출 테스트 진행
  3. SET(software test development engineer)는 개발 초기에 중형 테스트를 하나의 개별 기능으로 넣어 완료 되게 한다.
  4. SWE(software development engineer)는 실제 테스트를 작성하고, 디버깅하고, 관리한다.
  5. TE(test engineer)는 자동화가 어렵거나 비용(cost)가 많이 들 때 수동으로 수행한다.
 
 
- 대형 테스트 (제품이 사용자가 기대한대로 동작하며 원하는 결과를 내놓나)
  1. 3개 이상의 기능과 실제 사용자 시나리오와 데이터 소스를 다루며 몇 시간 이상 수행
  2. 결과 주도적이며 사용자 요구 사항을 만족키시는지 확인
  3. 자동화 -> 탐색적테스트 까지 모든
 
* 테스트는 개발 프로세스 그 자체로서의 부분으로 자리잡아야 함
* 품질 =/ 테스트 , 품질 = 개발 + 테스트
* 구글에서는 개발채널 -> 테스트 채널 -> 베타 채널 or 릴리스 채널로 서버 구분
* 테스트 명칭을 일반적으로 사용하는 "코드 -> 통합 -> 시스템" 대신 "소형 -> 중형 -> 대형"으로 지칭

- 앱의 종류
  1. 네이티브 앱 : 디바이스 엑세스 가능, PC 접근 불가능 ex) 올리브영 app
  2. 하이브리드 앱 : 네이티브 앱에 웹 뷰를 보여주어 웹 앱을 실행 ex) 네이버, 다음, 구글
  3. 모바일 웹 : 브라우저로 URL을 이용 디바이스 엑세스 불가능
  4. 웹 앱 : 모바일에 중점을 두고 개발(모바일 웹 + 네이티브앱), pc와 모바일 등의 기기 상관없이 똑같이 보임
 
 * 구글의 차세대 테스트 엔지니어링 틀의 설계 방향 : '사람이 인지할 수 있는 최대 범위' 안에서 최대한 자동화
