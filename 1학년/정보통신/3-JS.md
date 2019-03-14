선린인터넷고등학교 소프트웨어과 정보통신 과목 JS
======

소스 코드 위치
------
* 인라인

    * html 태그 속성 값에 js 코드 입력

* <script>태그 내부

    * html파일에서 script 태그 내부에 js 코드 입력

* 외부 파일

    * js파일을 생성한 후, 해당 파일에 js 코드 입력

    * <script src = "file.js"></script> 로 import


인라인 예제
------
* 수업에 사용한 이벤트 리스너

    * onclick

        * 마우스 클릭

    * onmouseover

        * 마우스를 올렸을 때

    * onmouseout

        * 마우스를 내렸을 때


&lt;img onclick = "alert('1');"&gt;

식별자
------
* 첫 번째 문자 : 알파벳, 언더스코어, 달러기호 사용 가능

* 두 번째 이후 : 알파벳, 언더스코어, 달러기호, 숫자 사용 가능

* 대소문자 구분

* 예약어 사용 불가

데이터 타입
------
* 숫자 타입 : 정수/실수 모두 표현 (number)

* 논리 타입 : true, false (boolean)

* 문자열 : 문자/문자열 모두 표현 (string)

* null : 값이 비어있음

* undefined : 값이 할당되지 않음

* 참조 타입 : 객체, 배열, 함수 등등

변수
------
* 값을 저장하는 공간

* var 변수명 = 초기값;

* 리터럴에 따라 데이터 타입이 동적으로 결정

* 지역 변수

    * 함수 내에 선언

    * 함수 내에서만 사용

* 전역 변수

    * 함수 밖에 선언

    * 프로그램 전역에서 사용

* this

    * 자신을 생성한 객체를 지칭

상수
------
* 값이 안바뀜 - 데이터 그 자체

* 문자열 상수

    * 이중 인용 부호, 단일 인용 부호 모두 사용

    * 이스케이프 문자

        * \b 백스페이스

        * \t 탭

        * \n 줄바꿈

        * \\\" 이중 인용 부호

        * \\\' 단일 인용 부호

        * \\\\ 백슬래시


연산자
------
* 산술 연산

    * \+ 더하기

    * \- 빼기

    * \* 곱하기

    * / 나누기(실수)

    * % 나머지

* 증감 연산자

    * ++(1증가)

    * --(1감소)

* 비트 연산자

    * & and
    * | or
    * ^ xor
    * ~ not
    * &lt;&lt; 왼쪽 시프트
    * &gt;&gt; 부호 전파 오른쪽 시프트
    * &gt;&gt;&gt; 부호 전파 오른쪽 시프트

* 대입 연산자

    * = 대입

    * +=, -= ... 산술 복합 연산

    * &=, ^=, |=, &lt;&lt;=, &gt;&gt;=, &gt;&gt;&gt;= 비트 복합 연산

* 비교 연산자

    * == 같은지 비교(형 변환)

    * != 다른지 비교(형 변환)

    * === 같은지 비교(형 변환x)

    * !== 다른지 비교(형 변환x)

    * &gt;, &lt;, &gt;=, &lt;= 크기 비교

* 논리 연산자

    * && and

    * || or

    * ! not

* 삼항 연산자

    * 조건?실행1:실행2 조건이 참이면 실행1, 거짓이면 실행2


다이얼로그 창
------

##### document.write(content);

* 인자 값을 html에 작성

##### 경고 다이얼로그

* alert(content);

* 인자 값을 경고창에 출력

##### 프롬프트 다이얼로그

* prompt(메시지, 기본값);

    * 반환 값은 입력 값

##### 확인 다이얼로그

* confirm(메시지);

    * 반환 값은 true, false

함수
------
##### 함수 즉시 실행
```javascript
( function() {
//내용
} () );
```

##### 수식, 코드 실행
```javascript
eval(par1str);
```

##### 문자열 -&gt; 10진 정수로 변환 후 리턴
```javascript
parseInt(par1str);
```

##### 인자가 NaN이면 true
```javascript
isNaN(par1obj);
```

객체
------
* property 객체의 고유한 속성(변수)

* method 함수. 객체 내부의 프로퍼티 값을 조작하거나 연산을 수행하고 결과 리턴

* js => 객체 기반 언어(캡슐화, 상속, 다형성 완벽하지 않음)


브라우저가 제공하는 js 객체
------
* 코어 객체(내장 객체)
  * 어디서나 사용 가능한 기본 객체
  * 엔진에 내장
  * 배열(Array), 날짜(Date), 문자(String), 수학(Math) 타입
* 문서 객체
  * HTML 문서에 작성된 각 HTML 태그를 객체화
  * HTML 문서의 내용과 모양 제어
* 브라우저 객체
  * 브라우저 제어를 위한 객체
  * 브라우저에 계층 구조로 내장
  * window screen location history 등


코어 객체
------
##### 코어 객체 생성
* new 키워드 사용
```javascript
var today = new Date();
var msg = new String("Hello");
//today와 msg는 레퍼런스 변수
//객체가 생성되면 객체 내부에 프로퍼티와 메소드 존제
```

##### Array 객체
* 여러 개의 원소들을 연속적으로 저장
* 전체를 하나의 단위로 다루는 데이터 구조
* 길이 선언 필요 x

* 리터럴 선언
```javascript
var arr = [];
```
* 객체 선언
```javascript
var arr = new Array(); //빈 배열
var arr = new Array(size); //크기 설정
var arr = new Array(data1, data2, ...) //초기화
```
* join(par1str)
	* 각각의 원소를 인자값으로 연결해 문자열로 반환 (원본 데이터 불변)
* reverse
	* 배열을 뒤집어 반환
* sort
	* 오름차순 정렬
* slice(par1int, par2int)
	* [par1, par2) 범위 반환 (원본 데이터 불변)
* splice(par1int, par2int [, par3obj] )
	* par3 생략 시
		* par1부터 par2개 삭제
	* par3 생략 안할 시
		* par1부터 par2개를 par3으로 fill
* concat(par1arr)
	* 현재 배열에 par1을 붙여서 리턴 (원본 데이터 불변)
* pop()
	* 마지막 데이터 삭제 후 반환
* push(par1obj)
	* 배열 맨 뒤에 데이터 삽입
* shift()
	* 첫 데이터 삭제 후 반환
* unshift(par1obj)
	* 첫 번째 인덱스에 데이터 삽입

##### Date객체
* new Date() //현재 날짜 시간
* new Date(year, month, date, hour, min, sec, ms)
* getFullYear()
	* YYYY
* getMonth()
	* month-1
* getDate()
	* date
* getDay()
	* 0~6 (sun~sat)
* getHours()
	* 0~23 (h)
* getMinutes()
	* min
* getSeconds()
	* sec
* getMilliseconds()
	* ms
* getTime()
	* 1970.1.1 0:0:0 기준 ms

##### String객체
* 생성자 사용
``` javascript
var str = new String("something")
```

* 리터럴 사용
``` javascript
var str = "something";
```
* []
  * 랜덤 액세스
* length()
  * 길이 반환(readonly)
* charAt(par1int)
  * par1에 있는 문자 반환
* charCodeAt(par1int)
  * par1에 있는 문자의 유니코드 반환
* concat(par1str, par2str, ...)
  * par1뒤에 par2, ... 연결 후 반환 (원본 불변)
* indexOf(par1str [, par2int] )
  * par2부터 par1가 처음으로 나타나는 인덱스 반환(par2 생략시 처음부터, 없으면 -1 반환)
* replace(par1str, par2str)
  * par1을 par2로 변경 후 반환 (원본 불변)
* split(par1str [, par2int] )
  * par1로 나눈 결과를 배열로 반환 (par2는 반환하는 배열의 크기 제한)
* match(par1str)
  * par1과 일치하는 문자열을 찾아 반환 (없으면 null)
* substr(par1int [, par2int] )
  * par1부터 par2개의 문자 반환 (par2 생략시 끝까지)
* substring(par1int, par2int)
  * [par1, par2) 범위 반환 (음수는 0으로 간주, par1/par2 크기 상관 없음)
* slice(par1int [, par2int] )
  * [par1, par2) 범위 반환 (par2 생략시 끝까지, 뒤에서부터 검색시 음수 사용, par1<par2)
* trim()
  * 문자열 앞뒤 공백 제거한 결과를 반환
* toLowerCase
  * 모두 소문자로 변환 후 반환
* toUpperCase
  * 모두 대문자로 변환 후 반환
