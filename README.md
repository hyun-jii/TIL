# TIL ( Today I Learned )
- 매일 배운 것을 간략히 기록  

## 2022-06-17(FRI). 
webflux CORS, CSRF, Headers. 

https://docs.spring.io/spring-security/reference/reactive/exploits/headers.html.  


## 2022-05-30(MON). 
Optional 바르게 사용하기  
https://homoefficio.github.io/2019/10/03/Java-Optional-%EB%B0%94%EB%A5%B4%EA%B2%8C-%EC%93%B0%EA%B8%B0/  

## 2022-05-13(FRI). 
webflux 의 Mono, Flux 는 Service 에서 발생한 exception을 throw 해도 Controller 에서 Exception 을 잡을 수 없다.  

## 2022-05-12(TUR). 
@Transient, @ReadOnlyProperty. 

## 2022-02-17(TUR).   
@JsonInclude. 
https://junho85.pe.kr/1626. 

Jackson 어노테이션  
https://ckddn9496.tistory.com/71  



brew install docker / brew install -cask docker.   
https://stackoverflow.com/questions/40523307/brew-install-docker-does-not-include-docker-engine/43365425#43365425  


spring boot 2.4 profile.  
http://honeymon.io/tech/2021/01/16/spring-boot-config-data-migration.html.  
https://spring.io/blog/2020/08/14/config-file-processing-in-spring-boot-2-4. 



r2dbc ReactiveCrudRepository, r2dbcEntityTemplate. 

## 2021-10-20(WED). 
eureka locator enabled. 
https://www.appsdeveloperblog.com/spring-cloud-api-gateway-automatic-mapping-of-routes/. 

## 2021-08-20(FRI). 
vue 에서 computed 에 비동기 처리  
https://github.com/foxbenjaminfox/vue-async-computed  

## 2021-07-15(TUR). 
Vue 의 template 에 object 속성을 바인딩 한 후, 속성을 변경하면 Vue 는 속성의 변화를 감지할 수 없기 때문에 re-rendering 이 이루어지지 않는다.  
그러므로 변경된 데이터값이 제대로 바인딩 되지 않는다.  
속성의 변화를 감지하려면 object 자체를 변경하거나, `Vue.set(object, key, value)` 를 사용하여 변경된 속성에 반응성을 추가할 수 있다.  
https://kr.vuejs.org/v2/guide/reactivity.html  

## 2021-02-03(WED)   
angular에서 checkbox의 체크 해제를 컨트롤 할 때 ng-model이 boolean이 아니라면,  
`ng-true-value` `ng-false-value` 를 활용할 수 있다.  
https://docs.angularjs.org/api/ng/input/input%5Bcheckbox%5D

## 2021-01-07(TUR)  
window === $window  
$(window) === angular.element(window)  
document !== $document  
$(document) === $document  
angular.element(document) === $document  

## 2020-11-13(FRI)  
git stash 후, stash 한 것을 잃어버렸을 때  
`git fsck --no-reflog`  
`git show SHA-1 코드`  
`git stash apply SHA-1 코드`  
https://nochoco-lee.tistory.com/218  

## 2020-09-14(MON)  
ngChange 와 ngClick 의 차이  
`ngChange` 는 호출되는 순간 상태 값이 변한다.  
반면 `ngClick`은 click이라는 동작 그자체이며, 상태값은 별도로 변경해야 변한다.   

## 2020-08-24(MON)  
`scope: false` 인 경우 디렉티브의 scope가 없기 때문에, 모두 scope가 같다. 그러므로 getter, setter 접근 시 $scope로 접근하면 된다.    
그러나 하나의 디렉티브 `scope: true` 인 경우 getter, setter 가 부모 scope에 선언되어 있으므로,  
상속받은 디렉티브에서 getter, setter를 사용할 때는 `$scope.$parent`로 접근해야 한다.  

## 2020-08-21(FRI)  
`scope: false` - no scope로 뷰와 directive가 바라보는 scope가 같다.  
변경사항이 즉시 반영된다.  
`scope: true` - inherited scope로  부모 스코프를 상속받으며, 자식 스코프에서 부모스코프 접근 시, no scope 보다 안전하다.  
no scope는 값이 원치 않게 바뀔 수 있기 때문에..?  
`isolated scope` - 독립적인 scope로 

## 2020-08-11(TUE)  
- setTimeout : 일정 시간 간격 후에 함수가 한번 실행  
- setInterval : 일정 시간 간격으로 함수가 주기적으로 실행  
setTimeout과 setInterval을 중지시키기 위해서는 clearTimeout과 clearInterval 을 사용한다.  
setInterval 보다 재귀적인 setTimeout 이 더 유연하다.  

## 2020-08-03(MON)  
함수 표현식, 함수 선언식  
https://hyun-jii.github.io/2020/2020-08-30-first/  

## 2020-07-30(TUR)  
@, =, &  
optional 은 `?`  

## 2020-07-29(WED)  
angularJs 에서 커스텀 디렉티브를 element로 구성할 경우,  
`template` 또는 `templateUrl` 이 꼭 필요하다.  

## 2020-07-28(TUE)  
angularJs 사용자 정의 디렉티브 생성 참조  
http://www.nextree.co.kr/p4850/  

## 2020-06-25(TUR)  
_.forEach, _.each  

## 2020-06-23(TUE)  
JSON.stringify  
ng-value , value  

## 2020-06-22(MON)  
_.filter  
_.some  
_.every  
_.cloneDeep  
_.set  
https://ui.toast.com/weekly-pick/ko_20190515/  
https://lodash.com/docs/4.17.15#prototype-value  

## 2020-06-03(WED)  
nodeJs에서 제공하는 assert 에서 strict 사용을 권장한다.  
`const assert = require('assert').strict`  
위와 같이 사용하면, equal() 이나 deepEqual()을 strict 모드로 바꿔준다.  
deepEqual()만 써도 deepStrictEqual()를 쓰는 것과 같다.  
`equal(), strictEqual()` , `deepEqual(), deepStrictEqual()`  
객체 비교를 할 경우에는 equal()를 사용하면 테스트가 실패한다.  
객체의 참조만을 비교하고, 객체 내부를 비교하지 않기 때문이다.  
그래서 `deepEqual`를 사용하는데, 이는 객체 내부도 같이 비교한다.  
https://hyunseob.github.io/2016/05/09/assert-nodejs-test-module/  

## 2020-05-27(WED)  
exec(), lastindex, slice()  
replace()는 정규식을 사용하지 않으면, 첫번째 해당되는 것만 replace  

## 2020-05-26(TUE)  
git stash, git stash pop, git branch  
https://jhhwang4195.tistory.com/4  

## 2020-05-22(FRI)  
리눅스 시스템에서 한줄의 끝이 `LF`로 이루어지고,  
윈도우에서 `CR`(Carriage Return)과 `LF`(Line Feed)가 합쳐진 `CRLF`로 이루어진다.  
터미널에서 이와 같은 오류가 발생하면, Git 협업으로 인한 Whitespace 에러이다.  
다음과 같은 방법을 해결하기 위해서는  
`git config --global core.autocrlf true`  
프로젝트에만 적용하고 싶을 때는 --global 옵션 해제  
단반향 변환은 다음과 같다.  
`git config --global core.autocrlf true input`  
변환하지 않고, 에러 메시지만 끄고싶다면  
`false`를 입력한다.  
module.exports, exports    

## 2020-05-15(FRI)  
`gulp` 란 node.js 기반의 task runner 이다.  
반복적이고 귀찮은 작업이나, 프론트엔드 빌드에 필요한 작업들을 쉽게 처리할 수 있다.  
ex) 코드 작성 -> Javascript Test -> Javascript Minify -> Javascript Merge  
-> CSS Minify -> CSS Merge  
위와 같은 일을 gulp 로 해결 가능  
`pm2` 란 노드 프로세스 매니징 도구 -> 터미널 환경에서 node의 관리 용이  
[참조](https://medium.com/harrythegreat/pm2-node-js-%EC%84%9C%EB%B2%84%EB%A5%BC-%EB%8D%94-%EC%89%BD%EA%B2%8C-%EA%B4%80%EB%A6%AC%ED%95%98%EA%B8%B0-1-12d30b0fedbe)    

## 2020-05-10(SUN)  
`Base64` 는 인코딩 방식을 의미한다.  
Basic 인증 방식에 쓰이는데, `Base64` 인증은 복호화가 가능하기 때문에 보안이 취약하다.  
그러므로 https / tls 와 함께 사용해야 한다.  
javascript 에서 `btoa()` 인코딩 하는 메소드 `atob()`는 디코딩 하는 메소드이다.  

## 2020-04-24(FRI)  
AJAX는 `promise` 객체를 내장하고 있어서,    
`then()` 을 활용하여, ajax 실행이 끝난 후 다른 메소드를 실행할 수 있다.  

## 2020-04-14(TUE)  
Javascript 에서 ajax 실행 후 다른 메소드 실행 시, 별도 처리를 하지 않으면  
두 메소드가 동시에 실행되어, 원하는 결과 값이 나오지 않는다.  
이 때 callback 을 사용할 수 있는데, callback은 callback 지옥에 빠지기 쉬우므로  
promise를 사용하여 처리하는게 더 좋다.  

## 2020-04-09(TUR)  
RestController, ResponseBody  

## 2020-04-08(WED)  
JSONArray와 JSONArray 연결은 `addAll` 메소드를 사용한다.  
`[{ }, { }, { }]` 형식의 파싱은  
`Object`로 파싱한 후 `JSONArray`로 캐스팅한다.  
그리고 반복문을 통해 `JSONObject` 생성  
`["key"[{},{}]]`    
`JSONObject` 파싱 후 `JSONArray`로 캐스팅한다.  

## 2020-03-28(SAT)  
톰캣 서버 구동 시 콘솔에 한글 깨짐 현상 해결  
톰캣 설치 폴더에서 `/conf/logging.properties` 파일에서  
`java.util.logging.ConsoleHandler.encoding = UTF-8` 을 주석 처리 한다.  
로그를 영어로 변경하기 위해선 톰캣 설정의 `VM options`에  
`-Duser.language=en -Duser.region=US`를 추가 한다.  

## 2020-03-24(TUE)  
`int`형은 제한은 21억이다. 반면 `BigInteger`의 범위는 무한대이다.  
1부터 100까지의 곱을 연산하는 결과는 굉장히 크기 때문에 BigInteger에 담아야한다.  
`BigInteger a - BigInteger.ZERO;` 다음과 같은 형식으로 사용한다.  
ZERO는 0, ONE은 1, TEN은 10으로 초기화 하는 것이다.  
1부터 100까지의 곱을 연산했으므로, ONE으로 초기화하고 연산하였다.  
연산은 BigInteger의 `multiply`메소드를 활용하였다.  
그리고 int형을 BigInter형으로 변환하는 것은 `BigInteger.valueOf()`이다.  

## 2020-03-17(TUE)  
하둡이란? 분산 환경에서 빅 데이터를 저장하고, 처리할 수 있는 자바 기반의 오픈 소스 프레임워크  
하둡패키징으로 `HDFS`, `맵리듀스`가 있다.  
HDFS는 하둡 분산형 파일시스템으로 데이터를 저장하는 분산형 파일시스템,    
맵리듀스는 대용량 데이터 처리를 위한 분산 프로그래밍 모델이다.  
맵은 연관성 있는 데이터들로 분류하는 작업을 하고,  
리듀스는 맵에서 출력된 데이터들 중 원하는 데이터를 추출하는 작업이다.  

## 2020-03-16(MON)  
오라클에서 문자열을 날짜로 포맷하는 것은 `TO_DATE('2020-03-16','YYYY-MM-DD')`  
MySQL에서는 `STR_TO_DATE('2020-03-16','%Y-%m-%d')` 이다.  
 
## 2020-03-07(SAT)  
이클립스에서 프로젝트 import 후 톰캣 실행 시, 톰캣이 프로젝트를 인식하지 못한다면  
`properties -> Project Factes` 에서 `Dynamic Web Project`를 체크해준다.  

## 2020-03-02(Mon)  
배포 스크립트 작성 후 배포 실행 시 계속 `Invalid or corrupt jarfile` 이라는 에러가 떴다.  
아무리 생각해도 여러번 배포로 생성된 여러개의 jar파일이 존재하여 jar파일을 못읽어오는 것 같았다.  
그래서 찾아보니 스크립트 부분에서  
`JAR_NAME=$(ls -tr $REPOSITORY/ | grep *jar | tail -n 1)` 이 부분에서  
`*jar` 가 문제였다..ㅠㅠ jar파일이 하나일때는 상관없지만 여러개의 jar 파일이 존재할 경우  
grep jar로 써주어야 한다. 아무래도 마지막 jar파일 하나만 가지고 오는 명령어랑 충돌이 되는 것 같다.  

## 2020-02-23(SUN)  
리눅스에서 로컬 서버 열린 포트 확인하는 방법 `netstat -tnlp`    
해당 서버 죽이기 `kill -15 PID`  

## 2020-02-22(SAT)  
- CI 와 CD  
`CI(Continuous Integration)`는 지속적인 통합으로, 자동으로 테스트와 빌드가 수행되어, 안정적인 배포파일을 만드는 과정이다. ex) TravisCI    
`CD(Continuous Deployment)`는 위 빌드 결과를 자동으로 운영 서버에서 배포까지 진행되는 과정이다. ex) CodeDeploy  

## 2020-02-18(TUE)  
- IaaS(Infrastructure as a Service)  
기존 물리 장비를 미들웨어와 함께 묶어둔 서비스로, 가상머신, 스토리지, 네트워크 운영체제 등의 IT인프라를 대여해주는 서비스이다.  
AWS의 EC2와 S3가 IaaS 이다.  
- Paas(Platform as a Service)  
아이아스보다 더 많은 기능을 제공해주는 서비스 이다.  
AWS의 빈스톡, 헤로쿠등이 있다.  
- Saas(Software as a Service)  
소프트웨어 서비스이다. 개발이 아닌 직접 사용하는 서비스이다.  
구글 드라이브, 네이버클라우드가 이에 속한다.  

## 2020-02-09(SUN)  
Mustache란?  
수많은 언어를 지원하는 가장 심플한 템플릿 엔진이다.  
템플릿엔진은 서버템플릿엔진, 클라이언트템플릿 엔진으로 나눌 수 있다.  
서버템플릿엔진은 예를 들어 JSP, 클라이언트템플릿 엔진은 Javascript라고 할 수 있다.  
Mustache는 Mustache.js와 Mustache.java 두 가지 모두 존재하여, 하나의 문법으로  
서버와 클라이언트템플릿 모두 사용 가능하다.  
로직코드를 사용할 수 없어서 뷰의 역할과 서버의 역할을 명확히 구분가능하다.  

## 2020-02-05(WED)  
Javascript 의 var, const, let의 차이점  
var는 hoisting 문제로 인해 잘 쓰이지 않고, 현재 const 와 let을 사용한다.  
var는 변수의 재 선언이 가능했지만, const와 let은 변수의 재선언이 불가능하다.  
let은 변수의 재할당은 가능하고, const는 변수의 재할당 재선언 모두 불가능하다.  

## 2020-01-22(WED)  
깃허브에서 파일을 잘못 올렸을 경우, 이를 레파지토리에서 삭제하고 gitingore로 관리하고 싶다면  
git rm 을 이용하면 된다. git rm 을 이용하여 전체 또는 해당 파일을 원격 저장소에서 삭제 할 수 있고,  
삭제한 후, gitignore에 관리하고 싶은 파일을 추가한다.  그 후 git add를 실행한 후, commit 과 push를 해주면  
파일이 더이상 원격 저장소에 올라가지 않는다. 하지만 히스토리는 지워지지 않는다.  

## 2020-01-16(THU)  
CRESCENDO 프로젝트를 AWS EC2 서비스를 이용한 배포와 RDS 서비스를 이용하여 디비 서버를 연결하려고 했다.  
AWS를 처음 사용해본지라 배포 과정이 까다롭고 어려운 부분이 많아 아직 도전중이다.  
우선 RDS로 데이터베이스 인스턴스를 생성하여 오라클과 연동하는 것은 비교적 간단하였다.  
하지만 프리티어 이용하다보니 어떻게 돈이 나갈지 몰라서 꾸준히 모니터링중이다....  

## 2020-01-04(FRI)  
> 한 페이지 내에서 자식창의 데이터를 받아 부모창에 데이터를 뿌려주는 작업을 했다. 에이젝스를 통해 처리하였는데  
> ajax 부분에 location.reload()를 사용하여 리스트를 새로고침 할 생각이었다.  
> 하지만..무슨일인지 insert문이 계속 실행이 되는 것이다..이게 대체 무슨일인가 보니..  
> Controller 부분에 insert처리부분과 리스트를 처리해주는 것을 한번에 하고 있었다.. 분리했어야하는데..  
> 이렇게 구성하다보니 redirect 처리도 잘 되지않았다..앞으로 잘 분리해야겠다..  


## 2019-12-31(TUE)  
> 마이바티스에서 insert 문 수행시, 시퀀스를 컬럼으로 사용하는 경우가 있다.  
> 이때, insert문 수행 직후 시퀀스의 값이 필요할때가 존재한다. 이때 맵퍼부분에서 selectKey를 선언해주면 된다.  
> currval을 통해 방금 실행된 insert문의 시퀀스 값을 가져올 수 있다.  
> 이걸 몰랐을 때 insert문 직후에 vo 설정도 해보고 여러방면으로 고생을 했는데 selectKey라는 간단한 방법을 통해 값을 추출할 수 있었다.  

## 2019-12-30(MON)  
> 마이바티스 쿼리문에서 부등호를 쓸 수 없다. 부등호 대신 &lf; &gt; 등을 사용하여 부등호를 표현하면 에러가 해결된다.  


## 2019-12-29(SUN)  
c:if 나 c:when 쓸때 조건을 두개 이상 주고 싶다면 ${state == 'total' && sort =='popular'}  이와 같이 하나의 ${} 안에 구성해야한다.  
${state == 'total'} && ${sort == 'popular'} 이와 같이 구성하면 안된다.  

## 2019-12-26 (TUR)  

디비 insert에 필요한 값을 form에서 전달받을 경우, 시퀀스 컬럼은 선언하면 안된다.    
시퀀스는 값을 전달받지 않아도, 쿼리문에서 시퀀스명.nextval로 생성되기 때문이다.  
예를 들어 prj_num 컬럼이 시퀀스인데, 이를 form 태그안에서 넘겨주었을 경우, prj_num 데이터가 제대로 들어오지 않는다.  


## 2019-11-15 (FRI)  
> - Spring Framework의 개념에 대해 배웠다.  
>   Framework 란 쉽게 말해 환경, 틀, 약속이며, Spring의 가장 핵심적인 철학은 다른 Framework들을 포용한다는 것이다.  
>   아직 개념적으로만 접근해서 잘 와닿지 않아, 빨리 활용해 보고 싶다.  


## 2019-10-31 (THU)  
> - JSP를 이용하여, 게시판 구축을 해보았다.  
>   게시판 리스트, 글 작성, 리스트에 글을 클릭했을 경우 나타나는 글 페이지, 글 수정과 삭제를 처리하고, 데이터들을 가져와서
>   처리하는 것을 적용하니 헷갈리는 부분이 많았다.    
>   특히 페이징부분 처리 연산이 많이 헷갈렸다.   
>   

## 2019-10-10 (THU)  
> - JDBC 설정


## 2019-09-30  (MON)  
- PL/SQL 트리거, 패키지  

## 2019-09-28  (SAT)  
- [프로그래머스 2016년](https://github.com/hyun-jii/Programmers/commit/957e6cacab6ca9194b93a8eab790d62de456f92a)  
> Calendar Class의 set함수를 통해 년,월,일을 설정할 수 있다.  

## 2019-09-27  (FRI)  
- PL/SQL 프로시저, 트리거  

## 2019-09-25  (WED)  

- PL/SQL  
> PL/SQL 문법( IF, FOR LOOP, LOOP, WHILE LOOP등)  
> FUNCTION 정의  
> PL/SQL 문법이 자바와 SQL 문법의 중간의 느낌이었다. 그래서 익숙했지만 문법들이 둘이 섞여서 많이 헷갈렸다.  

## 2019-09-24  (TUE)  

- [HR 스키마 ERD 기반 테이블 복사](https://github.com/hyun-jii/Oracle)    
> 기존의 테이블의 정보(제약조건, 참조, PRIMARY KEY등)을 수집하여, 기존의 테이블과 똑같은 테이블들을 생성  
> 7개의 테이블들이 서로를 참조하고 있어, 이 관계를 파악하고 참조순으로 테이블을 생성하였다.  
> 이 과정에서 한 테이블이 자기 자신을 참조할 수 있다는 것을 알게되었고,
> 제약조건을 잘못 설정하면 제약조건을 지우고 다시 추가 해야했다.  

## 2019-09-23 (MON)  

- 정규화
> 제 1정규형, 제 2정규형, 제 3정규형, 제 4정규형, 역정규화에 대해 배웠다.  
> 정보처리기사 시험을 본 뒤 배우니 더욱 이해가 잘 되었다.  
> 그리고 무결성과 제약조건, 제약조건별 컬럼 레벨의 형식과 구조, 테이블 레벨의 형식과 구조를 배웠다.
> (제약조건 : PRIMARY KEY, FOREIGN KEY, UNIQUE, CHECK, NOT NULL)  















