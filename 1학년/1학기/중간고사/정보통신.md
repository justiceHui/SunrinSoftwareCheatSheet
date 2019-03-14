선린인터넷고등학교 소프트웨어과 정보통신 과목 HTML
======

기본틀
------
<pre>
<code>
  &lt;!DOCTYPE html&gt;
  &lt;html&gt;
    &lt;head&gt;
      &lt;meta charset = 'utf-8' /&gt;
      &lt;title&gt; title &lt;/title&gt;
    &lt;/head&gt;
    &lt;body&gt;

    &lt;/body&gt;
  &lt;/html&gt;
</code>
</pre>

특수문자
------
* 따옴표 - &amp;quot;
* &amp; - &amp;amp;
* 띄어쓰기 - &amp;nbsp;
* &lt; - &amp;lt;
* &gt; - &amp;gt;

강조
------
* b 태그 - 볼드체
* strong 태그 - 볼드체 + 강조
* i 태그 - 이탤릭체
* em 태그 - 이탤릭체 + 강조
* mark 태그 - 형광펜
* del, s 태그 - 취소선

인용
------
* q 태그 - 인용, 들여쓰기x
* blockquote 태그 - 인용, 들여쓰기o

Ordered_List
------
* &lt;ol&gt;
* 속성
  * type - { {숫자, 1}, {대문자, A}, {소문자, a}, {대문자 로마, I}, {소문자 로마, i} };
  * start - number
  * reversed - boolean
* &lt;li&gt;
  * 항목 추가

Unordered_List
------
* &lt;ul&gt;
* &lt;li&gt;
  * 항목 추가

Definition_List
------
* &lt;dl&gt;
  * 설명 목록
* &lt;dt&gt;
  * 제목
* &lt;dd&gt;
  * 설명

anchor
------
* &lt;a&gt;
* 속성
  * href (Hyper REFerence) - "주소"
  * href (Hyper REFerence) - "#아이디"&nbsp;&nbsp;&nbsp;&nbsp;->&nbsp;&nbsp;&nbsp;&nbsp;&lt;태그 id = '아이디'&gt;
  * target - { {새 창, _ blank}, {현재 창(default), _ self} }

image
------
* &lt;img&gt;
* 속성
  * src - 링크
  * alt - 사진 뜨지 않을 때 대체용
  *  height width - 크기 조절 (하나만 정하면 비율에 따라 자동 조절)

<pre><code>
&lt;figure&gt;
  &lt;img asdf&gt;
  &lt;figcaption&gt;&nbsp;&nbsp;&nbsp;&nbsp;설명&nbsp;&nbsp;&nbsp;&nbsp;&lt;/figcaption&gt;
&lt;/figure&gt;
</code></pre>

table
------
* &lt;table&gt;
  * 테이블 만들기
* &lt;tr&gt;
  * 행 만들기
* &lt;td&gt;
  * 셀 만들기
* &lt;th&gt;
  * 제목 셀 만들기 (굵게, 셀의 중앙에 배치)
  * &lt;caption&gt;&nbsp;&nbsp;&nbsp;&nbsp;&lt;caption&gt;
    * 설명
* 속성
  * border 속성 - 테두리
  * rowspan - 상하 셀 병합
  * colspan - 좌우 셀 병합


audio
------
* &lt;audio&gt; &lt;/audio&gt;
* 속성
  * src 재생할 오디오가 존재하는 URL 지정
  * autoplay 자동재생
  * controls 오디어 재생 제어기 표시
  * loop 반복재생
  * preload 미리 다운로드 -&gt; 빠르게 재생 가능
<pre>
none 미리 다운로드 안함
metadata 메타 정보만 다운
auto 전체 미리 다운로드
</pre>
*  &lt;source&gt; (audio태그 내부에서)
  * src 주소 지정
  * type
<pre>
audio/mp3 - 음성 압축
audio/wav - 윈도우 표준 사운드 포멧, 파일 용량 큼
audio.ogg - 오픈소스개발
</pre>

<table>
<tr> <th>브라우저</th> <th>mp3</th> <th>wav</th> <th>ogg</th> </tr>
<tr> <th>인터넷 익스플로러</th> <td>O</td> <td>X</td> <td>X</td> </tr>
<tr> <th>크롬</th> <td>O</td> <td>O</td> <td>O</td> </tr>
<tr> <th>파이어폭스</th> <td>O</td> <td>O</td> <td>O</td> </tr>
<tr> <th>사파리</th> <td>O</td> <td>O</td> <td>X</td> </tr>
<tr> <th>오페라</th> <td>O</td> <td>O</td> <td>O</td> </tr>
</table>

video
------
* &lt;video&gt; &lt;/video&gt;
* 속성
  * src, dautoplay, controls, loop, preload
  * poster 재생전, 재생 불가시 표시
  * muted 소리 끔
  * width, height
* &lt;source&gt; (vidio태그 내부에서)
  * src 주소지정
  * type
<pre>
video/mp4 - 적은 용량으로 고품질 구현
video/webm - 무료, 고화질 영상 압축
video/ogg - 무료, 비디오 압축 기술
</pre>

<table>
<tr> <th>브라우저</th> <th>mp3</th> <th>webm</th> <th>ogg</th> </tr>
<tr> <th>인터넷 익스플로러</th> <td>O</td> <td>X</td> <td>X</td> </tr>
<tr> <th>크롬</th> <td>O</td> <td>O</td> <td>O</td> </tr>
<tr> <th>파이어폭스</th> <td>O</td> <td>O</td> <td>O</td> </tr>
<tr> <th>사파리</th> <td>O</td> <td>X</td> <td>X</td> </tr>
<tr> <th>오페라</th> <td>O</td> <td>O</td> <td>O</td> </tr>
</table>

form
------
* &lt;form&gt;
  * 사용자 &lt;--&gt; 서버
* 속성
  * action - 데이터 처리하는 스크립트 주소 url
  * method - 데이터 보내는 방법 (get, post)

1. 웹브라우저가 포함된 웹페이지 로드
2. 입력
3. submit(전달)
4. 서버 스크립트로 처리, 응답

* get 방식
  * url 뒤에 파라미터 붙여서 전달
  * 2048자 제한
* post 방식
  * HTTP Request 헤더에 포함시켜 전송, 길이제한 없음
  * 전송 후 뒤로가기 누르면 다시 보내야 한다는 경고 뜸


form - input 태그
------
* &lt;input&gt;
* 속성
  * type - 유형
  * value - 초기값
  * name -요소 이름
  * autofocus - 페이지 로드되면 자동으로 포커스
  * placeholder - 입력 필드에 힌트메시지 표시
  * readonly - 읽기 전용 필드
  * required - 반드시 채워져야 하는 필드(제출시 검사)

### type
* text
  * 기본 크기 20
  * size 로 크기 조절
* password
  * 비밀번호 입력창
* radio
  * 라디오 (동그란 버튼, 하나만 선택 가능)
  * name, value 반드시 속성 지정 필요 (같은 name끼리 그룹으로 취급)
  * 서버에는 "name"="value" 형태로 전달
  * checked - 기본값
* checkbox
  * 여러 개 동시 선택 (사각형 버튼)
  * name 속성이 동일해야 함
  * checked - 기본값
* submit
  * 데이터를 서버로 전송
* reset
  * 입력 필드 초기화
* file
  * accept속성 - 허용하는 파일 형식 지정 ( ex - image/* )
  * enctype = "multipart/form-data" 추가
* hidden
  * 입력은 아니지만 클라이언트가 서버에 특정 데이터를 전송
  * 화면 변화 없음
  * 서버에 name, value 전송
* button
  * onclick = "자바스크립트"
  * value = "버튼 내용"
* image
  * 제출 버튼 역할
  * src = "url" alt = "제출버튼"
* HTML5 FORM - search
  * 검색 상자
  * 오른쪽에 x 기호
* HTML5 FORM - email
  * 이메일 주소 입력
  * required 속성 - 유효한 이메일 주소인지 검사 (제출시 검사)
* HTML5 FORM - number
  * 숫자 입력
  * max, min, step 속성
  * value속성 - 초기값
* HTML5 FORM - range
  * 슬라이드 막대로 숫자 지정
  * max, min, step 속성
  * value속성 - 초기값
* HTML5 FORM - date
  * Y M D입력
* HTML5 FORM - datetime-local
  * 날짜, 시간 입력(지역 표준 시간대)
* HTML5 FORM - month
  * Y M입력
* HTML5 FORM - week
  * Y 주 입력
* HTML5 FORM - time
  * 시간 입력
* HTML5 FORM - color
  * 색상 입력

### form - button 태그
* &lt;button&gt;&nbsp;&nbsp;내용&nbsp;&nbsp;&lt;/button&gt;
  * 버튼 안에 텍스트, 이미지 삽입 가능
* type 속성
  * submit
  * reset
  * button

### form - textarea 태그
* 속성
  * rows(세로 사이즈), cols(가로 사이즈) 속성
  * name 속성

### form - select 태그
* 메뉴 표시
* option태그와 함께 사용
  * value, selected 속성

### form - fieldset 태그
* 하나의 폼을 여러 구역으로 표시
* field태그 안쪽에 legend태그 - 제목 설정

### form - label 태그
* label 태그 안에 input 요소 넣기
<pre>
&lt;label&gt;학번 &lt;input type = "text"&gt;&lt;/label&gt;
&lt;label for = "id"&gt;학번&lt;/label&gt;
</pre>

시맨틱 태그
------
* 시맨틱 웹 : 웹 페이지에서 사람이 인식하는 정보를 기계가 이해할 수 있게 하는 기술
  * 이름만 봐도 문서 구조에서 어떤 역할을 하는지 알 수 있음
* header
 * 머리말
 * 검색창
 * 사이트 메뉴
* footer
  * 제작자 연락처
  * 저작권 정보
* nav
  * 문서 연결 링크
  * 네비게이션 메뉴
* section
  * 주제별로 구분
  * h1 ~ h6 태그와 같이 사용
* article
  * 실제 내용
  * 독립적 글 표시
* aside
  * 사이드바
  * 메인 내용에 영향 x
* address
  * 주로 footer 안에서 사용
  * 제작자 정보
* iframe
  * inline frame
  * 다른 페이지 삽입
  * 속성 - src, width, height, name, seamless(테두리제거)
<pre>
    &lt;iframe name = "window"&gt;대체텍스트&lt;/iframe&gt; &lt;br&gt;
    &lt;a href = "https://jhnah917.xyz" target = "window"&gt;바로가기&lt;/a&gt; &lt;br&gt;
    &lt;a href = "http://jhnah917.dothome.co.kr" target = "window"&gt;바로가기2&lt;/a&gt;
</pre>


div태그
------
* divide
* 블록 레벨 요소 (항상 새 줄에 시작하고 사용할 수 있는 전체 폭을 차지)
* 콘텐츠를 논리적인 섹션으로 분리하여 시각적 효과를 적용할 때 사용

span태그
------
* 인라인 레벨 요소 (필요한 크기만 차지)
* 텍스트 일부의 스타일 속성 설정

주의
------
<pre>
단일 태그 : &lt;br&gt; &lt;hr&gt; &lt;meta&gt; &lt;input&gt; &lt;source&gt; &lt;img&gt;
</pre>
