## 전자정부 표준프레임워크 커스터마이징 

***
### 커스터 마이징 후 파스타 클라우드 활용예정(공통)
1. 스프링프로젝트 kimilguk_egov 변경 -> kimilguk-egov.
2. 이클립스에서 kimilguk-egov 프로젝트를 파스타에 배포.(Mysql용)
3. kimilguk-egov 프로젝트용 클라우드 DB생성: 서비스명은 egov-mysql-db.
4. 파스타 클라우드에서 egov-mysql-db의 원격접속이름과 암호를 확인.
5. 이미 생성된 phpmyadmin 애플리케이션명: kimilguk-myadmin 실행.
6. http://kimilguk-myadmin.paas-ta.org 접속후 전자정부 프로젝트용 더미데이터 인서트.
7. http://kimilguk-egov.paas-ta.org 사이트에서 파스타 배포결과 확인. 
***

[공지] QR출결앱 사용(아래)
최초에 입실버튼을 누르면 입실버튼이 확인버튼 으로 바뀝니다. 
매 쉬는시간마다 확인버튼 으로 체크하시고 
마지막 퇴실시에만 퇴실 버튼 누르면 됩니다.

### 다음주 예정
- 과제물 제안요청서 pptx파일 리뷰.
- 전자정부 프로젝트 AdminLTE용 답글쓰기 기능 추가.
- 애플리케이션 설계 pptx문서 마무리.

### 20200904(금)-아래
- view.jsp 에서 파일다운로드 기능 사용하기 위해서 수정한 파일명은
- src/main/webapp/WEB-INF/jsp/cmm/fms/EgovFileList.jsp 에서 <a 링크 부분 추가 처리.
- 첨부파일 있을때, 수정시 에러 발생(다운로드 부분때문에)
- 왼쪽메뉴 active 풀리는 것 방지용 수정: footer.jsp 하단 var current = '${bdMstr.bbsId}';
- 예전 오라클프로젝트(HomeController클래스)에서 게시판 타입을 셋션으로 처리
  session.setAttribute("세션게시판_변수네임", "값변수");//세션변수 생성
  session.getAttribute("세션게시판_변수네임");//세션변수 보기
- insert.jsp 파일에서 fn_egov_addBoard() -> fn_egov_insertBoard() 변경.
- src/main/java/egovframework/let/cop/bbs/web/EgovBBSManageController.java 파일 참조.
- addBoard(입력화면) , insertBoard(DB입력처리) 기존 2개로 나누어짐.
- insertBoard(입력화면), addBoard(DB입력처리) 우리것을 위 기존 네이밍으로 변경처리.
- 파일위치: src/main/webapp/WEB-INF/jsp/cop/bbs/EgovNoticeRegist.jsp
- EgovNoticeRegist.jsp 이파일에서 hidden값을 insert.jsp로 가져옵니다.
- 코드 인스펙션(소스 분석)_다른 솔루션 분석할때 사용하는 방법.
- BoardController.java 클래스에 매핑추가.
- 경로를 만들었으면, 매칭되는 View(jsp)와 매칭시키는 것을 = @Requestmapping(컨트롤러추가) 
- 게시판 생성 버튼 클릭 처리. 매개변수=파라미터=인자=쿼리스트링=질의문자
- 9월17일 부터는 보드(노드MCU-C언어)+라즈베리파이(Raspberry Pi-gcc사용) 사용 고민됩니다.
- 게시판관리 메뉴 분리 후 2개 모두 선택문제 처리(JQuery로 문제점 처리) 유지보수 비용
- 기존 공지사항/갤러리 관리로 메뉴를 분리처리.
- 전자정부 프로젝트 AdminLTE 신규게시물생성, 답변게시물생성까지 작업 예정 입니다.
- it강의 저장소의 애플리케이션 설계의 구글 프레젠테이션 문서도 변경 했습니다. 이용하셔도 됩니다.
- 학습목차에 올려놓은 사항은 지웠습니다.
- 작업기준은 아래 변경된 문서로 작업 하시면 됩니다.
- 구글 프레젠테이션 문서 변경했습니다.-> 변경 한 것으로 작업해 주세요...
- 변경한 파일 위치는 it강의 저장소 > 학습목차 제일하단에 다운로드 할 수 있습니다.
- 데이터전송관련된: Soap 프로토콜, Http 프로토콜
- RestAPI설계문서 작업은 예전 했던 화면에 보이는 OpenApi.java 프로그램을 기준으로 함.
- 개발자라고해서 꼭 코딩만 하지 않습니다. 위 화면처럼 지루한 문서작업도 합니다.
- 전산화=SI업체가 하는일 = 오프라인 작업 -> 온라인으로 변경하는 주 작업.
- 전자정부 프로젝트 공통모듈 > 일정관리 기능 3가지 ( 월별, 주간별, 일별 일정보기 )
- 오프라인 일정관리(엑셀,프린트종이,벽에거는 화이트보드) -> 온라인 일정관리로 변경
- 다음주 월, 요구사항 확인(제안요청서pptx) 잘하신 분들 리뷰예정.
- 전자정부 프로젝트 공통모듈 > 배너관리 기능(CRUD) > 배너새성, 조회, 수정, 삭제
- MVC구조란 ( Model:데이터베이스, View: jsp화면, Controller: Model단과 View단 매칭)
- @애노테이션 클래스종류: @Controller, @Service, @Repository, @Inject, @Resources, @Autowired ...

### 20200903(목)-아래
- 이론예정: 전자정부 일정관리 기능(모듈) 기능 상세명세 확인 + 기능유형이름 확인.
- 이론예정: 모델2 의 MVC에 대해서 확인.
- 이론예정: MVC기반의 애노테이션 종류 확인.
- 내일은 전자정부 프로젝트 AdminLTE 신규게시물생성, 답변게시물생성까지 작업 예정 입니다.
- 방과후 2차 시험예정.
- 오늘 나머지 시간은 타 시스템 연동 오픈RestAPI설계 부분 문서작업 진행해 주시기 바랍니다.
오늘 전자정부 프로젝트 AdminLTE 삭제기능 에러 나신분 원격지원해드릴동안
다른 학생들은 아래 문서 작업진행 하십니다. 주작업은 문서위주작업입니다.

### v11 애플리케이션 설계 수업진행은 아래 2가지로 진행.

#### 1. 아래쪽은 문서화 작업.
- 타 시스템 연동: Hrd-Net API이용해서, 구직자 훈련과정 콘솔창에 출력하는 자바프로그램 제작했습니다.
- 위 작업 URL: http://www.hrd.go.kr/hrdp/ap/papco/PAPCO0700T.do
- 타 시스템 연동했던 프로그램을 문서화하는 작업이 이전 주(40시간) 메인작업 내용내용.
- 문서작업시 Rest Api Status code 내용 기록.
- 이클립스에서 소스위치: 프로젝트명/src/test/java/kr/or/test/OpenApi.java 참조.

#### 2. 아래쪽은 이론 서술형 내용.
- 공통 모듈 인덱스 및 기능 코드 설계. 전자정부 개발버전 3.9버전 상세 가이드>
- 정보제공/알림>배너관리>배너관리 기능설명(CRUD), 
- 배너관리에서 관련소스 유형(Controller, Service, ServiceImpl, Model, VO, DAO, xml쿼리)
- 공통컴포넌트란? 업무처리로직에 +관리자관리모듈 +게시판관리모듈 레고블록처럼 추가 개발.
- 공통컴포넌트(모듈) 중에 게시판관리 변경(삭제부분-완전삭제로 변경), 관리자관리 기능 추가.
- 3-1프레임워크적용방안>아키텍처 규칙
- Annotation(애노테이션기반)@-스프링MVC준수: @RequestMapping(URL 매핑처리)
- 대표적인 애노테이션 클래스: @Controller, @Service, @Repository
- 확장 = extends = 상속 같은 의미, 다른말.
- 지금 우리가 개발하는 전자정부 프로젝트는 연계구축에 해당됩니다.
  통합DB(전자정부-ibatis,AdminLTE-mybatis) 때문에 지금 작동됩니다.
- 참고자료문서에서 
- 2-6프레임워크구성>최적의 공통컴포넌트 개발을 위한 필요조건(아래)
  1)UML기반산출물표준화+2)명확하고알기쉬운설계+3)재사용이쉬운설계(클래스사용)
  +테스트기반의개발(애자일)+생명주기기반의서비스제공

- 재사용성 확보하기 위한 공통모듈: 전자정부 프로젝트의 게시판, 일정관리, 회원관리
- UML(유니버셜 마크업 랭귀지): 유스케이스때 사용된 액터 같은 기호(예,졸라맨)를UML이라고 함.
- 오후는 애플리케이션 설계 과목 입니다.
- 시험 보시느라 수고 많으셨습니다.^^
- 4교시 시험 시작 합니다.(이미지수정시 서명란 입력 부탁드릴께요)
- 제출물은 평가자체크리스트이미지+사후평가이미지+과제물pptx파일+시간.jpg

- xml쿼리-서비스(DAO)-현재컨트롤러에서 실행처리-@Inject 인스턴스변수 생성 후 호출OK.
- 전자정부프로젝트인증조건 extends상속 EgovComAbstractMapper필수
- 임플리먼트 패키지 안쪽에 DAO클래스(@Repository포함)생성.
- 인터페이스 만드신 후 임플리먼트 패키지에 BoardServiceImpl클래스 생성.
- 서비스클래스에 @Service 애노테이션을 붙이면, 스프링빈으로 등록
- 서비스패키지 만듭니다. du.human.com.board.service->인터페이스생성
- 쿼리가 완성 되었으니, 자바폴더에서 서비스(DAO포함)만듭니다.
- 테이블명 대문자로 해 주세요(영역지정후 Ctrl+Shift+X 대문자로)
- mapper폴더안에 board폴더 생성 후 board_mysql.xml삭제쿼리 생성
- xml쿼리생성(mybatis사용)-DAO생성-Service생성-현재컨트롤러 수정
- 이후 기존코드유지 후 새 코드 작성
- BoardController클래스 엽니다.
- 전자정부 프로젝트 AdminLTE게시판 삭제 기능 마무리

```
 오늘 과제물과 시험지 제출 방법.
- 1. Daum카페로 이동해 주세요.-시험지 이미지 다운로드.
- 2. 시험방법은 그림판에서 시험지 이미지에 서명추가 및 편집. 

```
4교시: 과제물+사후평가게시판에 업로드.
 - 4교시 업로드 파일3개 (문제지,사후평가,제안요청서pptx)
5교시: 사전평가게시판에 업로드.
 - 5교시 업로드 파일1개 (사전평가지)
우리반 이수자평가 예정되어 있습니다.
 - 외부평가인원이 오셔서 여러분 세 분을 무작위 선발해서 시험을 봅니다.
 - 교육이 제대로 되어있는지 외부 평가를 합니다.
 - 다음달에 선발된 세 분 학원에 나오셔서 외부평가인원에게 시험보게 됩니다.
 - 제가 주관하는 게 아닙니다. 저도 어제 이야기를 들었습니다.
 - 시험은 서술형 시험입니다.(더해서 외부평가인원의 면담 있습니다.)
 - 우리가 지금까지 봤던 종이 서술형 시험문제 중에서 나옵니다.
```

20200902(수)
- AdminLTE용 게시물 생성 기능 추가 합니다.(앞으로 v11애플리케이션 설계 시간 설계내용으로 실습예정)
- AdminLTE용 게시물 삭제 기능 추가 합니다.(오늘은 기존 삭제 기능 까지_앞으로 신규 완전삭제기능으로 추가)
- AdminLTE용 파일 다운로드 링크 추가 합니다.(EgovNoticeInqire.jsp 179라인)
- 기존 삭제 컨트롤러 참조: EgovBBSManageController
- 관리자삭제: 완전하게 게시판 레코드를 삭제처리.
- 기존삭제: 기존-필드USE_AT 값을 N 으로 변경해서 삭제처리.
- flag(깃발) 달면 되지 않을까요?
- EgovNoticeUpdt.jsp 파일(기존egov파일) 참조: 하단 Js부분 복사
- 작성자는 필수 입력값 입니다. list.jsp에 있는 frstRegisterNm 복사합니다.
- form name="frm" -> "board" 로 변경
- readonly(폼전송에 포함), disabled(폼전송에서 제외)
- let(Light Enviroment Template):경량 환경 템플릿 약자
- 유효성 검사 항목을 분리처리( EgovNoticeRegist.xml파일 )
- 전자정부 프로젝트 유효성 검사에 사용되는 설정파일 확인(게시판유효성)
- 오전 수정 버튼 클릭시 작동않되었습니다. 이유는 input 태그에 name값이 없어서 입니다.
- view.jsp 파일, BoardController.java파일 2개 파일 수정했습니다.
- 업데이트에러 인데, 뭐가 누락되서 에러 나오는지 확인에 필요한
- 외부 라이브러리 사용 준비중...
- 유효성 검사때문에 수정.
- 기존 업데이트페이지명 EgovNoticeUpdt.jsp
- 2개의 페이지를(뷰+수정) -> 1개로 변경중(수정페이지 1개로)
- form 속성중에 multipart 부분이 누락되어서 않됨.
- <form></form> 변경: <form:form></form:form> 폼전송시 보안처리
- XSS(크로스사이트스크립트) 방지(해킹코드방지) 실행해킹코드를 
  실행불가능한 일반문자로 변경처리
- 이전 작업한 스프링 프로젝트에서는 redirect: 페이지 이동경로
- 전자정부 프로젝트는 forwoard: 페이지 이동경로
- 기존 컨트롤러 이용: egovframework.let.cop.bbs.web 패키지
- 참조 컨트롤러명: EgovBBSManageController.java
- 이전 스프링 프로젝트는 수정을 별도의 페이지로 구성하였으나,
- 전자정부 프로젝트는 수정을 보기페이지와 같이 사용하도록 처리.
- 위 처리 내용 2가지 제목/내용 readonly 제거,작성자값 ntcrNm 변경
- 전자정부 프로젝트 실행-브라우저
- 에러 상화 처리 확인
- 나머지 학생들은 구글 요구사항 제안요청서 계속 작성해 주세요.

### 20200901(화) 
- 리스트에서 답글 표시 하는 방법(계단식)
  EgovNoticeList.jsp 참조.
- 답글 게시판의 로직은 스프링 코딩 상관없이 
  SQL 쿼리에서 해결하는 겁니다.- 5년-10년 전에는 게시판 과목
  제일 마지막 부분 답글게시판 이었습니다.
- 메서드-Method(자바에서 호칭 함수), 함수-Function(C언어/자바스크립트에서 사용)
- @ModelAttribute("searchVO") BoardVO boardVO 
  1. 컨트롤러가 받는 변수는 boardVO 확인 OK,
  2. jsp 로 보내는 변수는 searchVO 확인 OK.
- 이전 관리자기능은 전자정부에 없었기 때문에 우리 맘대로 만들었다면,
  지금 작업하는 게시판관리 기존전자정부에 있기 때문에 기존 규칙을 따른는 것이 안전함.
- 요구사항: 기존문제점-관리자단,사용자단 짬뽕 -> 개선사항: 관리자단/사용자단 분리 처리.
- 파일이름으로 검색할때 단축기 : Ctrl+Shift+R 조합 => Open Resource 창 띄우기
- 이전 스프링 프로젝트 만들때, 기본CRUD 만들고(Board), 추가한부분(BoardVO) = 검색기능+페이징기능
- BoardVO클래스(자식) > Board클래스(부) = 부모+자식 포함된 모든 변수(get,set) 다 사용.
- 학생들은 요구사항 확인 제안요청서 ppt 문서 계속 입력해 주시기 바랍니다.
- 부트스트랩 JQuery 그리드시스템 사용 가로 12개 = 6개 + 6개 분리(50%:50%)
  그리드 JQuery는 자동 계산식이 들어가 있습니다.col-4라면, 화면이 3개로 분할됨
  <div class="col-4" /><div class="col-4" /><div class="col-4" />
  33.3333% + 33.3333% + 33.3333% = 100%로 처리(반응형처리 됨)
  그리드(격자,모눈종이 12개 가로 칸을 가지는 모눈종이) 12개 가로화면 분할
- placeholder 옵션은 입력 힌트로서 회색으로 표시됩니다.
- 호출하는 곳은 list.jsp 에서 호출(링크)
  지금까지 작업내용 확인, 브라우저에서...
- BoardMasterVO master = new BoardMasterVO();//인스턴스 클래스변수 만들기.
  Get,Set 사용하기위해서 인스턴스ㅡ 변수 만든이유 입니다.
- 기존 패키지에서 egovframework.let.cop.bbs.web >
  EgovBBSManageController.java > > selectBoardArticle.do 매핑값 복사 196라인 참조
- 기능별로 나눠져 있는 방식을 따라서 edu.human.com.board.web 패키지에 추가.
- view.jsp 디자인 확인: 컨트롤러에서 @RequestMapping 경로 추가...
- 카드 클래스 : card 웹 프로그램에서 최초로 사용하던곳 쇼핑몰에서 상품을 겔러리 형식으로
                표시할때 사용하던 방식.(카드방식)
- 이클립스 작업은 여기까지 하시고, ppt 제안서 작성을 진행 하시기 바랍니다.
- 게시판 상세보기 화면 만들고, 프로그램 입히기 작업진행 중...
- 기존프로젝트에서 board_view.html 파일 찾아서 테이블 디자인 입히기.
- 이클립스 내장된 브라우저는 이쁘게 나오지 않습니다.(크롬에서 보시면 정상으로보임)
- 1. 전자정부 프로젝트 제안요청서 계속 작성
- 2. 전자정부 프로젝트 이클립스 띄워서 지금까지 작업물 확인(아래)
     AdminLTE 관리자단 > 게시판관리 > 검색어(공지1) 로 검색해서 1개 출력

```
[공지] QR출결앱 사용(아래)
최초에 입실버튼을 누르면 입실버튼이 확인버튼 으로 바뀝니다. 
매쉬는시간마다 확인버튼 으로 체크하시고 
마지막 퇴실시에만 퇴실 버튼 누르면 됩니다.
```
- 37. 나머지 학생들은 ppt 문서 계속 입력해 주시고, 원격 프로그램셋팅 필요하신 분 제게

``` 
    화면 공유 요청 해 주시고, 일단 한혜성 씨 부터 요청해 주세요...
    현재 한혜성씨 화면 제어 하는 부분을 보여 드리겠습니다.
    화면 공유 하실때 화면1 네...
```

#### 전자정부 프로젝트 제안서 작성방법

- 36. 납품완료시 : 전자정부 프로젝트 소스 + ERD + 테이블정의서 + 매뉴얼 + 사이트배포 내용을 DVD로 구워서 고객사에게 전달해주어야 합니다.

- 35. 구글 ppt문서에서 [***학생이 작성] 부분은 학생이 작성하는 부분 입니다.
    
 ```   
    애자일 프로그래밍의 대표적인 방법 2가지
    - 익스트림 프로그래밍 : 구글 (2인1조 프로그래밍)- 1개소스를 2명이 작업하는 방식.
    - 스크럼방식 : 쉽지가 않습니다.(8명정도 모아놓고, 1개 프로그램을 진행)
  하다보면 1인 주도 개발이 됩니다.
```
- 34. 애자일(Agile) -  테스트주도(TDD) 개발 방법론: Hot 유행어

```
    단위프로그램개발 -> 테스트 -> 피드백 -> 수정 -> 테스트 -> OK -> 다음 단위프로그램개발
```
- 33. Mysql의 특징

```
    관계형데이터베이스-RDBMS, 오픈소스(단, 커뮤니티버전), Ansi(표준)-SQL사용,
```
- 32. 스프링 웹프로그램 실행모델

```
    위 이미지 부분를 다른 이미지로 대체.
    디스패쳐서블렛: 서블렛(자바프로그램)배치 = 스프링폴더> context-servlet.xml
    (뷰리졸버-뷰단jsp해석기 포함)
```
- 31. 스프링프레임워크란?

```
    특징을 기록(MVC사용, 오픈소스, DI(인젝션사용), AOP(인터셉터사용), OOP(클래스사용)
    서블렛(10년전+고전클래스-오리지널 자바로) 
       -> 스트럿츠(5년전+OOP클래스) -> 스프링(현재+MVC+DI+AOP)
```
- 30. 우리가 리뉴얼하는 전자정부-egov프로젝트는 오픈소스 입니다.(무료배포)

```
    사용자/개발자 입장에서 돈 투자없이 시간만 들이면, 상품이 만들어 집니다.
    자본없고, 사람있고, 기술있는 우리나라에서는 괜찮은 수익 창출 방법 입니다.
    그래서, 오픈소스를 사용한 컨버전스(융합) 기술이 대세입니다.
    우리반이 디지털 컨버전스(융합)반 - 오픈소스 사용이 대세 입니다.
    오픈소스 돈 버는 방법: 작업 대행해 주는 방법으로 수익을 창출합니다.
    오픈소스로 만들어진 프로그램은 무료(돈받고 팔 수없습니다.) 단, 작업비는 받을 수 있다.
```
- 29. 산업표준을 지향: 애플, MS, 오라클, 구글 = 본인이 표준이 되면, 돈이 됩니다.
- 28. 3티어 구조:

``` 
    소프트웨어 단 : Model(Db) - View(화면) = 2티어 구조
                    Mode(DB) + Controller(URI매핑) + View(사용자화면) = 3티어 구조(MVC)
    하드웨어 단: DB서버1 + 웹서버1 = 서버 2티어 구조
                 서버1(웹서버+DB서버) = 1티어 구조
```
- 27. 프로그램 결과 출력: 이부분은 전자정부 프로젝트 -egov 프로젝트 AdminLTE        관리자관리부분 캡쳐

- 26. CMS가 왜 중용하냐하면? 그래서, 중요합니다.

```
    모든 웹프로그램은 CMS가 포함되어 있습니다.
    백엔드: 자바스프링 프로그램도 예외가 없습니다.
    프론트엔드: CMS많이 사용됩니다.
    CMS없는 웹프로그램은 없다고 보시면 됩니다.
```
- 25. 웹프로그램 도움말은 글로만 만드시는 게 아닙니다.
    위 화면처럼 이미지캡쳐 하시고, 간단한 코멘트 다는 것으로 매뉴얼이 만들어 집니다.

- 24. C언어로 만드는 구구단 프로그램 작성 후 실행
    
- 23. 라즈베리파이(*손바닥컴퓨터) 와 노드MCU(마이크로 컨트롤 유닛)라는 아두이노 개발보드

```
    원격으로 실습을 진행하는 방법을 고민 중입니다.
    9월17일(보름 후)날 필요하니까, 코로나19 때문에 원격으로 한다면, 고민중입니다.
```
- 22. C언어: gcc 컴파일러 사용(자바는 javac)

```
    gcc -o(옵션) hello(실행파일명) main.c(소스명) -l(링크옵션:외부라이브러리 가져오기)
    내장함수만으로 실행이 않될때, 외부 함수를 불러다 사용할때 -l (link)링크옵션입니다.
    앞으로 라즈베리파이 회로판에 발광다이오드(LED) 2개를 깜박이게 하는 소스(아래)
    gpio-led.c 파일
   ```
- 21. 개발에 사용되는 서버환경, 개발환경 및 실행 환경, 오픈SW명 작성

```
    전자정부표준프레임워크에서 참조: 
    CI:지속적인 소스 통합 / DI: 배포방식 통합 => 개발 파이프라인
    Jenkins 2.190.1: 예정 파스타 클라우드(젠킨스): 파이프라인 사용시 써보았습니다.
    서브버전 대신 => 깃허브 사용
```
- 20. 도움말 부분은 관리자관리 기능 사용법 기록(이미지 캡쳐로 도움말 대체)

- 19. 라이센즈 정책 적는 목적은 여러분이 오픈소스라이센스를 알고 있는지 확인용도

```
    GPL, Apache, LGPL, MIT 등 
    자바(OpenJDK 8), Mysql-커뮤니티버전(개인용무료), 스프링프레임워크(찾아서 기록)
    전자정부표준프레임워크(아파치 2.0 라이센스)
    필요한 이유: 취업한 회사에서 오픈소스를 사용하기 때문에...
```
- 18. 메인페이지 (AdminLTE 메인페이지 넣으시면 됩니다.)
  egov 프로젝트 캡쳐이미지

- 17.
 
```
내일 전자정부-egov 프로젝트 진행에 문제가 있으신분은 오늘 오후 7시 카톡주시면
    원격으로 봐드리겠습니다.(주말 여러학생분이 요청하셔서 바로 처리 되었습니다.)
    보통 20분내에 실행 가능하게 셋팅 됩니다.
```
- 16. 기존 javascript(네이티브 자바스크립트-오리지널 JS-구형 JS)

``` 
 -> JQuery사용
    기존: document.getElementById("요소이름-div").value;
    Jquery: $("요소이름-div").val();
```
- 15. 코딩시 학생분이 손들고 화면공유 요청 하시면, 제가 원격으로 접속하게 됩니다.

```
  원격작업화면은 여러분들에게 여기 화면에 같이 공유하도록 하겠습니다.
  에러 상황은 어떻게 처리하는지 모두 확인 가능 하시리라 생각 됩니다.
```
- 14. 타이틀은 전자정부 기존 심플홈템플릿을 리뉴얼 하기.

```
 전자정부 kimilguk-egov 프로젝트 작업하시던 내용을 시나리오에 적으시면 됩니다.
 기존 전장정부 심플 홈템플릿 문제점: 디자인이 html4, 사용자와 관리자가 한화면 포함.
 개선 사항 시나리오: html4->html5(AdminLTE사용), 관리자단 분리(/admin/home.do)
 위 제안요청서 ppt 문서에 기록하시면 됩니다.
 잘 구글 프레젠테이션 문서 잘 정리 하셔서, 면접보실때, 포트폴리오 제출시 같이 제출
 하시면, 좋은 점수를 받지 않을까 합니다.
```
- 13. CMS( 콘텐츠 관리 시스템 ): 간단하게는 게시판을 말합니다.

``` 
 제품: 웹하드(출력소에서 주사용-유료), 워드프레스(오픈소스-미국), 
 그누보드(오픈-국산)
 구글클라우드, 네이버클라우드.
```
- 12. 프로토타입 도구: 대표적으로 [카카오 오븐] 이 프로토타입도구 입니다.
	목적: 피드백 받기 위해서(개발자, 고객, 사용자에게)

- 11. 채팅창에 출석이라고 해 주시기 바랍니다. 캡쳐예정 입니다.
- 10. 모두 자리에 앉으시고, 카메라 켜 주시기 바랍니다.
카톡 공지사항 있습니다.
- 9. 시간 더 필요하신 분 손 들어주세요
- 8. PDF문서 42페이지 부터 진도 시작 입니다.
- 7. 지난주에 진도 나가던 부분을 열어 주세요.(화면에서 확인)
- 6. 화면처럼 체크 후 다운로드 해주세요.
- 5. 화면하단 NCS학습모듈 > 1. 요구사항 확인 > PDF 버튼을 클릭해 주세요.
- 4. 01.정보기술 > 02.정보기술개발 > 02.응용SW엔지니어링 선택해 주세요.
- 3. 정보통신을 클릭해 주세요
- 2. 버전 10.0.0 화면하단의   NCS학습모듈 로 들어가주세요
- 1. 깃 it 강의 저장소로 이동해 주세요

### 20200820(목) 작업(아래)
- 3). 진도에 맞춰서 수업진행.
- 2). 전자정부프로젝트(스프링)를 리뉴얼(AdminLTE디자인관리자단)작업.
- 1). 9월중순 아두이노 작업시 스케치프로그램(언어) 사용 하기전, C언어 미리보기
  구름IDE(온라인)으로 실습.
### 20200819(수) 작업(아래)
- 4). 클라우드 파스타 앱 제거 후, 이클립스 PUSH(???-egovadmin관리용 php앱 이름)
- 3). 클라우드 파스타 mysql서비스 제거 후, 생성(???-egov-db 서비스 이름)
- 2). 타일즈 템플릿(UI쪽-레이아웃정리) 라이브러리 사용. 전자정부 프로젝트에 적용OK.
- 1). DB인터페이스 확인 (아래)
- 실행가능한 소스 https://github.com/miniplugin/Dbinterface_ora_ok.git
 ( 오라클 insert 후 커밋, System.out.print(vo.toString()); )
### 20200818(화) 작업(아래)
- 2). 서버프로그램 시험준비 후 3교시 부터 시험.
- 1). 관리자 등록시 아이디중복체크(RestAPI사용) 마무리.
- 주). RestAPI사용은 이클립스 내장브라우저에서는 않되기 때문에, 크롬 또는 IE사용OK.
### 20200817(월) 작업(아래)
- 3). 전자정부 프로젝트*(관리자관리기능추가한것) 파스타에 배포.(시간날때처리)
- 2). 관리자 등록시 아이디중복체크(RestAPI사용) 기능추가.
- 1). 관리자관리 기능 CRUD 마무리 OK.

### 20200814(금) 작업(아래)
- 3). 로컬PC에서 결과 확인 후 파스타에 배포예정.
- 2). 멤버 뷰페이지, 업데이트페이지, 인서트 페이지 생성.

```
우리가 기존에 작업한 스프링 프로젝트에서 아래처럼
<form id="폼이름" name="폼이름">
</form>
전자정부 프로젝트에서는 아래처럼
<form:form commandName="폼이름" name="폼이름">
</form:form>
```
- 1). 컨트롤러에 멤버리스트페이지 경로추가(아래)
- edu.human.com.member.web 패키지생성(컨트롤러용 패키지)
- MemberController.java @Controller클래스 생성.
- com/member/selectMember.do 경로추가(아래)
- 0). 관리자관리 경로 com/member/selectMember.do 로그인체크 추가
  로그인체크 관련 파일: egov-com-servlet.xml(서블렛파일) 인터셉터 관리
  뷰리졸버(viewresolver): 뷰단(jsp)단 해석기계.(웹페이지루트, 확장자 지정)

```
/**
 관리자관리 목록을 조회한다.
*/
@RequestMapping("/com/member/selectMember.do")
public List<EmployerInfoVO> selectMember(Model model) throws Exception {
	model.addAttribute("resultList", 멤버서비스호출);
	return "com/member/list";
}
```

### 20200812-13(수-목) 작업내역(아래)
- 6). jsp폴더(뷰폴더)에 inc/EgovIncLeftmenu.jsp 파일수정

```
메뉴 내용 추가(아래)
<li class="dept02"><a href="javascript:fn_main_headPageAction('57','com/member/selectMember.do')">관리자관리</a></li>
```
- 5). viewMember 쿼리+DAO+Service매서드 추가 후 Junit테스트OK.
- 4). Junit 테스트로 CRUD 확인.
- 3). Service 클래스에서 insertMember, updateMember, deleteMember 매서드 생성
- 2). DAO 클래스에서 insertMember, updateMember, deleteMember 매서드 생성
- 1). 쿼리 생성 : src/main/resources/egovframework/mapper/com/member/member_mysql.xml

### 20200811(화) 작업내역(아래)
- Junit 테스터로 DAO의 selectMember 실행 하기.

```
3. egov-com-servlet.xml 파일에서 component-scan 부분에서 제외된(exclude)를 -> 포함시킴(include)
2. src/test/java/~/TestMember.java 추가함. @ContextConfiguration 경로가 2개 추가.
1. 전자정부 프로젝트는 기본 Junit이 없기 때문에, 테스트환경 만들어야 함.. Pom.xml에 junit 모듈 추가하기.
```
- DAO(@Repository), Service(@Service) 만들기

```
3. service/impl/MemberServiceImpl.java (구현클래스) @Resource 대신 @Inject 사용
2. service/MemberService.java (인터페이스)
1. service/impl/MemberDAO.java (추상클래스를 사용, extends EgovAbstractMapper 필수 )
```
- 프로젝트에서 마이바티스 사용하기

```
4. 스프링-마이바티스 설정파일 추가: context-mapper.xml
- configLocation: 마아바티스 설정파일 위치 mapper-config.xml 추가
- mapperLocation: 쿼리가 존재하는 폴더위치 member_mysql.xml 추가(쿼리)
3. 관리자관리 테이블과 get,set 하는 VO 만들기: EmployerInfoVO.java
- 테이블 생성쿼리에서 필드명 복사 VO 자바파일에서 사용. 특이사항, 대->소문자 Ctrl+Shift+y 단축키
2. 관리자관리에 사용되는 테이블 확인 : emplyrinfo
1. 메이븐 모듈 추가(pom.xml)
<!-- 마이바티스 사용 모듈 추가 -->
<dependency>
	<groupId>org.mybatis</groupId>
	<artifactId>mybatis</artifactId>
	<version>3.2.8</version>
</dependency>
<dependency>
	<groupId>org.mybatis</groupId>
	<artifactId>mybatis-spring</artifactId>
	<version>1.2.2</version>
</dependency>
```
  
### 20200810(월) 작업내역(아래)
- context-datasource.xml: Hsql 데이터베이스 사용 주석처리

```
<!-- hsql -->
<!-- 여기만 주석처리
<jdbc:embedded-database id="dataSource-hsql" type="HSQL">
	<jdbc:script location= "classpath:/db/shtdb.sql"/>
</jdbc:embedded-database>
-->
```
- globals.properties :(주,유니코드 에디터로 수정) DB에 관련된 전역변수 지정(아래)

```
# DB서버 타입(mysql,oracle,altibase,tibero) - datasource 및 sqlMap 파일 지정에 사용됨
Globals.DbType = mysql
Globals.UserName=root
Globals.Password=apmsetup
# mysql
Globals.DriverClassName=net.sf.log4jdbc.DriverSpy
Globals.Url=jdbc:mysql://127.0.0.1:3306/sht
#Hsql - local hssql 사용시에 적용
#Globals.DriverClassName=net.sf.log4jdbc.DriverSpy
#Globals.Url=jdbc:log4jdbc:hsqldb:hsql://127.0.0.1/sampledb
```
- web.xml : 톰캣(WAS)가 실행될때 불러들이는 xml설정들 확인.

```
egov-com-servlet.xml(아래) 
- DispatcherServlet(서블렛배치=콤포넌트-scan:@Controller,@Service,@Repository에 관련된 설정 수정)
- <context:component-scan base-package="egovframework,edu">
- 위에서 ,edu 추가: edu.human.com패키지추가로 해당패키지로 시작하는 콤포넌트를 빈(실행가능한 클래스)으로 자동등록하게 처리
```
- pom.xml : 메이븐 설정 파일중 Hsql DB를 Mysql DB사용으로 변경(아래)

```
<!-- 주석처리
<dependency>
	<groupId>org.hsqldb</groupId>
	<artifactId>hsqldb</artifactId>
	<version>2.3.2</version>
</dependency>
 -->
<!-- mysql driver 주석해제 -->	
<dependency>
    <groupId>mysql</groupId>
    <artifactId>mysql-connector-java</artifactId>
    <version>5.1.31</version>
</dependency>

<!-- log4jdbc driver 주석해제. 기능:Console창에 쿼리보이기 -->        
<dependency>
    <groupId>com.googlecode.log4jdbc</groupId>
    <artifactId>log4jdbc</artifactId>
    <version>1.2</version>
    <exclusions>
        <exclusion>
            <artifactId>slf4j-api</artifactId>
            <groupId>org.slf4j</groupId>
        </exclusion>
    </exclusions>
</dependency>
```