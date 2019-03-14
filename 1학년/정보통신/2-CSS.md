선린인터넷고등학교 소프트웨어과 정보통신 과목 CSS
======

기본틀
------
<pre>선택자{속성 : 값; 속성 : 값;}</pre>

선택자
------
1. 타입 선택자 -&gt; 태그{...}
2. 아이디 선택자 -&gt; #아이디{...}  태그#아이디{...}
3. 클래스 선택자 -&gt; .클래스{...}  태그.클래스{...}
4. 가상 선택자 -&gt; 클래스가 정의된 것처럼 간주
5. 속성 선택자 -&gt; 특정한 속성을 가지는 요소 선택
6. 전체 선택자 -&gt; *{...} -&gt; 전체 선택

id - 하나의 요소만 가능
class - 여러 요소 가능
name - CSS에서 사용 불가

선택자 연습 - http://flukeout.github.io/

가상 선택자
------
a:link  방문하지 않은 링크

a:visited  방문한 적 있는 링크

a:hover  마우스를 롤호버 했을 때

a:active  마우스를 클릭했을 때

input:focus  텍스트 입력 칸에 커서를 둘 때

속성 선택자
------
h1[title] {...}
> h1태그 중 title 속성을 사용하는 요소
>> &lt;h1 title="asdf"&gt; ghjkl &lt;/h1&gt;

p[class="example"] {...}
> p태그 중 class속성의 값이 example인 요소
>> &lt;p title="example"&gt; ghjkl &lt;/p&gt;

선택자 - 우선순위
------
1. id
2. class
3. tag

같은 경우 -&gt; 아래가 우선

선택자{속성 : 값!important; } -&gt; 우선순위 무시

선택자 - 직계
------
s1 s2{...} -&gt; s1안에 있는 s2 선택(조상 자손)

s1 > s2{...} - &gt; s1의 직계 자식인 s2 선택(부모 자식)

CSS 위치
------
내부 스타일 시트 - head 태그 안에 css 작성

외부 스타일 시트 - 외부 파일에 .css 저장
> head 안에 &lt;link type = "text/css" rel = "stylesheet" href = "file.css"&gt;

인라인 스타일 시트 - 각각의 HTML태그 안에 스타일 지정
> &lt;h1 style="color:red&gt;asdf&lt;/h1&gt;

##### 부모의 속성은 자식에게 상속됨

CSS 위치 - 우선순위
------
1. 인라인

2. 내부

3. 외부

4. 웹브라우저 디폴트 값

CSS 속성 - font
------
<dl>
    <dt>font-family</dt>
        <dd>폰트의 종류(글꼴) 지정</dd>
        <dd>폰트 이름이 여러 단어이면 ""</dd>
        <dd>마지막은 일반적인 글꼴</dd>
        <dd>ex) serif sans-serif monospace cursive fantasy</dd>
        <dd>
            <dl>
                <dt>구글 폰트 사용</dt>
                    <dd>
                        ex) &lt;link href="https://fonts.googleapis.com/css?family=Libre+Barcode+39" rel="stylesheet"&gt;<br>font-family:"Libre Barcode 39", "궁서", serif;
                    </dd>
           </dl>
        </dd>
        <dd>
            <dl>
                <dt>웹 폰트 사용 (x)</dt>
                    <dd>https://www.web-font-generator.com/ 에서 ttf를 웹폰트로 변환<br>preview.html에서 @font-face 복사해서 style 태그 안에 붙여넣기</dd>
            </dl>
        </dd>
        <dt>font-size</dt>
         <dd>폰트 사이즈</dd>
            <dd>
                <dl>
                    <dt>절대 단위</dt>
                        <dd>pt, cm, mm, in, 키워드(xx-small, x-small, small, medium(디폴트), large, x-large, xx-large)</dd>
                    <dt>상대 단위</dt>
                        <dd>px(화면 해상도), %(부모 요소), em(부모 요소), rem(HTML요소)</dd>
                        <dd>12pt = 16px = 1em (일반적인 경우)</dd>
                </dl>
            </dd>
    <dt>font-weight</dt>
        <dd>글자 굵기</dd>
        <dd>100~900</dd>
        <dd>normal - 400</dd>
        <dd>bold - 700</dd>
        <dd>bolder, lighter</dd>
    <dt>font-style</dt>
        <dd>이텔릭체</dd>
        <dd>normal, itelic</dd>
    <dt>font-variant</dt>
        <dd>작은 대문자</dd>
        <dd>narmal, small-caps</dd>
    <dt>font</dt>
        <dd>폰트 축약 기법</dd>
        <dd>여러가지 속성을 한 줄에 설정</dd>
        <dd>
            <ol>
                <li>font-style</li>
                <li>font-variant</li>
                <li>font-weight</li>
                <li>font-size (필수)</li>
                <li>font-family (필수)</li>
            </ol>
        </dd>
        <dd>ex) font: italic small-caps 700 40px serif</dd>
</dl>

CSS 속성 - text
------
> 참고 : http://www.w3schools.com/css/css_colors.asp

<dl>
    <dt>color</dt>
        <dd>이름 "red"</dd>
        <dd>16진수 #ff0000</dd>
        <dd>퍼센트 rgb(100%, 0%, 0%)</dd>
        <dd>10진수 rgb(255, 0, 0)</dd>
    <dt>text-align</dt>
        <dd>center 가운데 정렬</dd>
        <dd>left 왼쪽 정렬</dd>
        <dd>right 오른쪽 정렬</dd>
        <dd>justify 양쪽 정렬</dd>
    <dt>text-decoration</dt>
        <dd>none 없음</dd>
        <dd>overline 윗줄</dd>
        <dd>line-through 가운데 줄</dd>
        <dd>underline 밑줄</dd>
    <dt>text-transform</dt>
        <dd>none 없음</dd>
        <dd>uppercase 대문자로 변환</dd>
        <dd>lowercase 소문자로 변환</dd>
        <dd>capitalize 단어 첫 글자를 대문자로</dd>
    <dt>text-shadow</dt>
        <dd>text-shadow : 가로거리 세로거리 번짐정도 색상</dd>
        <dd>, 로 연결 가능<br>ex) text-shadow : x1 y1 z1 red, x2 y2 z2 yellow</dd>
    <dt>word-wrap</dt>
        <dd>비(非)아시아 언어의 줄 바꿈</dd>
        <dd>normal 줄바꿈 적용x, 글자가 너무 길면 영역 밖으로 나감</dd>
        <dd>break-word 줄바꿈 적용o, 글자가 너무 길면 자동으로 단어를 잘라서 줄바꿈</dd>
        <dd>
            <pre>
                p{
                    border : 1px solid black;
                    width : 500px;
                    word-wrap : break-word
                }
            </pre>
        </dd>
    <dt>word-break</dt>
        <dd>아시아, 비 아시아 언어의 줄 바꿈</dd>
        <dd>break-all 글자 단위 줄바꿈</dd>
        <dd>keep-all 단어 단위 줄바꿈</dd>
        <dd>
           <pre>
                div{
                    border : 1px solid red;
                    width : 200px;
                }
                #breakall{word-break : break-all;}
                #keepall{word-break : keep-all;}
            </pre>
        </dd>
    <dt>다중 컬럼</dt>
        <dd>column-count 컬럼 개수</dd>
        <dd>column-gap 컬럼 사이의 간격</dd>
        <dd>column-rule 구분선 스타일</dd>
        <dd>
            <pre>
                p{
                    column-count : 2;
                    column-gap : 20px;
                    column-rule : 2px dotted red;
                }
            </pre>
        </dd>
    <dt>line-height</dt>
    <dd>줄 간격 지정</dd>
    <dd>normal 기본값</dd>
    <dd>숫자 글자크기 * 숫자</dd>
    <dd>백분율 글자크기 * 백분율</dd>
    <dd>@px</dd>
</dl>

css 박스 모델
------
* HTML요소들을 박스 형태로 간주하고 그리는 것

* 배치, 색상, 경계 속성

<pre>마진(margin){ 경계(border){ { 패딩(padding){ 컨텐츠(content) } } } }</pre>

### 경계
<dl>
    <dt>border-(top, right, left, bottom)-style</dt>
        <dd>none, dotted, dashed, solid, double, groove, ridge, inset, outset</dd>
    <dt>border-width</dt>
        <dd>경계선의 폭</dd>
        <dd>px / thin dedium thick</dd>
    <dt>통합</dt>
        <dd>border : width style color</dd>
        <dd>style 필수</dd>
    <dt>border-radius</dt>
        <dd>경계의 반지름 - 둥근 경계선</dd>
    <dt>box-shadow</dt>
        <dd>가로 세로 번짐 색상</dd>
</dl>

### 패딩, 마진

* content 크기 설정
<dl>
    <dt>요소 크기 설정</dt>
        <dd>width, height</dd>
        <dd>블록레벨 요소의 너비, 높이 설정</dd>
    <dt></dt>
</dl>

* margin : content 사이의 간격

* padding : border와 content 사이의 간격

* 컨텐츠 &lt; 패딩 &lt; 보더 &lt; 마진

* box-sizing: border-box;
> border를 포함한 크기 지정

#### margin, padding 크기 설정
1. 값 지정
<dl>
    <dt>auto</dt>
        <dd>브라우저가 자동으로 계산</dd>
    <dt>length</dt>
        <dd>px pt cm 지정</dd>
        <dd>기본값 0px</dd>
    <dt>inherit</dt>
        <dd>부모 요소 상속</dd>
</dl>

2. 크기 지정
> margin : 상 후 하 좌
>> 1개 : 전체
>> 2개 : 상하, 좌우
>> 3개 : 상, 좌우, 하

### 정렬
* 인라인 요소 정렬
> 인라인 요소를 포함하는 블록 요소에 text-align 사용

* 블록 요소 정렬
> margin의 left와 right를 auto로 지정

>> margin-left : auto; margin-right : auto;

### 배경
<dl>
    <dt>background-image</dt>
        <dd>url("경로")</dd>
    <dt>background-repeat</dt>
        <dd>repeat, repeat-left, repeat-right, no-repeat</dd>
    <dt>background-attachment</dt>
        <dd>scroll : 배경 요소와 같이 스크롤 (기본값)</dd>
        <dd>fixed : 배경이 뷰 포트에 대해 고정</dd>
    <dt>background-size</dt>
        <dd>이미지 크기 지정</dd>
        <dd>px, %단위(부모 기준)</dd>
        <dd>1개 : 전체 :: 2개 : 가로, 세로</dd>
    <dt>background-position</dt>
        <dd>배경 이미지 위치 설정</dd>
        <dd>x, y축 이동</dd>
        <dd>px, %단위</dd>
    <dd>{left, right, center}, {top, bottom, center} 조합</dd>
    <dt>background</dt>
        <dd>background : 색깔 이미지(링크) 반복 위치</dd>
</dl>

### 리스트 스타일
<dl>
    <dt>list-style-type</dt>
        <dd>마커 타입 지정</dd>
        <dd>circle(빈 원), disc(기본값, 원), square, upper-roman</dd>
    <dt>list-style-image</dt>
        <dd>url("경로")</dd>
    <dt>list-style-position</dt>
        <dd>outside(기본값)</dd>
        <dd>inside(들여쓰기)</dd>
    <dt>list-style</dt>
        <dd>list-style : 타입 이미지 포지션</dd>
</dl>

### 테이블 스타일
<dl>
    <dt>border</dt>
        <dd>테이블 경계 설정</dd>
        <dd>width style color</dd>
    <dt>border-collapse</dt>
        <dd>separate : 분리</dd>
        <dd>collapse : 통합</dd>
    <dt>background-color</dt>
        <dd>색깔 입력</dd>
    <dt>text-align</dt>
        <dd>정렬</dd>
        <dd>left, right, center</dd>
</dl>

css 레이아웃
------
* 레이아웃 : 웹 페이지에서 HTML 요소의 위치, 크기 결정

* 블록 요소
>화면 가로 폭 전체 차지

* 인라인 요소
> 현재 줄에서 필요한 만큼의 너비만 차지

> 한 줄에 차례대로 배치

### display 속성
* 블록, 인라인 설정
<dl>
    <dt>block</dt>
        <dd>블록 요소로 변경</dd>
    <dt>inline</dt>
        <dd>인라인 요소로 변경</dd>
    <dt>none</dt>
        <dd>없는 것처럼 간주</dd>
</dl>

### 위치 설정
* top, bottom, left, right 속성 사용

* position 속성 필수
<dl>
    <dt>static</dt>
        <dd>정상적인 흐름에 따른 위치</dd>
        <dd>블록 요소는 상하 배치</dd>
        <dd>인라인 요소는 한 줄에 차례로 위치</dd>
    <dt>relative</dt>
        <dd>정상적인 위치가 기준점</dd>
        <dd>본래 위치에 상대적으로 배치</dd>
    <dt>absolute</dt>
        <dd>컨테이너가 기준점</dd>
    <dt>fixed</dt>
        <dd>윈도우 원점이 기준점</dd>
        <dd>스크롤해도 위치 고정</dd>
</dl>

### float 속성

* 용도
> 이미지, 텍스트 함께 표시

> 레이아웃 설정

#### 이미지, 텍스트 함께 표시

* 부모 컨텐츠의 가장 왼, 오른 쪽으로 이동
> float : left, float : right

* 여러 번 적용
> 이전 요소에 이어서 표시

#### clear 속성
* float 속성 중단

* clear : right;

> float : right 중단

### z-index 속성
* 곂치는 요소의 스택 순서 지정

* 클수록 앞에 배치

* 기본값 : 0

### 요소 크기 지정
* min-width, min-height

* max-width, max-height

### overflow 속성
<dl>
    <dt>hidden</dt>
        <dd>벗어나면 안보이게 함</dd>
    <dt>scroll</dt>
        <dd>항상 스크롤바 표시</dd>
    <dt>auto</dt>
        <dd>부모 영역 벗어나면 스크롤바 표시</dd>
</dl>

css 효과
------

### opacity 속성
* 투명도 (0.0 ~ 1.0)

### visibility
* 가시성

* hidden, visible(기본값)

* display:none vs visibility:hidden

> display -&lt; 자리 차지x

> visivility -&lt; 자리 차지o

### transition
* transition : [전환의 대상이 되는 css속성] [전환 효과 지속 시간]

* 변경될 때 시작, 지속시간동안 fade in, out

<pre>
<code>
#a{
    background-color:red;
    transition: background-color 10s;
}
#a:hover{
    background-color:blue;
}
</code>
</pre>
