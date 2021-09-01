# 1.HTML
### 1.1_HTML이란
  * HyperText Markup Language
  * 웹 페이지의 생김새를 표현하는 마크업 언어
  * 마크업 언어: 여는 태그와 닫는 태그로 영역을 구분하는 언어
```
head : HTML의 머리부분, 현재 페이지의 설정을 정의하는 곳
body : 현재 웹 페이지의 화면에 보여지는 내용을 채우는 곳
title : 현재 웹 페이지의 제목, 웹 브라우저의 탭 이름으로 사용된다.
```
### 1.2_제목과 문단
  * 줄이 자동으로 바뀌는 태그 : 블록 요소
  * 줄이 바뀌지 않는 태그 : 인라인 요소
```
<p> : 블록 요소
<b> :인라인 요소
```
### 1.3_요소
   *	여는 태그와 닫는 태그와 그 사이의 내용을 모두 통틀어서 HTML요소라고 부른다
   *	br, hr처럼 닫는 태그를 생략 가능한 태그들도 있다
```
&lt; : 여는 태그
&gt; : 닫는 태그
i 태그 : 기울인 글꼴
b 태그 : 굵은 글씨
```
### 1.4_속성
   *	모든 요소는 속성을 가질 수 있다
   *	속성은 해당 요소의 여는 태그에 정의해야 한다
   *	속성을 통해 해당 요소의 추가적인 정보를 묘사할 수 있다
   *	대부분의 속성은 속성 이름과 속성 값이 짝을 이룬다
### 1.5_링크
   *	외부 페이지에 링크 걸기
```C
<a href="http://naver.com">네이버로</a>
<a href="http://comic.naver.com">네이버 웹툰으로</a>
```
* 페이지의 특정 부분으로 링크 걸기
  * 페이지 내부 원하는 요소의 ID속성을 이용하면 그 요소가 보이는 화면으로 링크를 걸 수 있다	
```C
<a href="#chap01">챕터1</a> <br>
```
### 1.6_이미지
   *	src 속성 : 출력하고자 하는 이미지의 경로
   *	alt 속성 : 해당이미지의 설명(이미지 출력 실패시 대신 출력됨)
   *	width 속성 : 해당 이미지의 너비 조절
   *	height 속성 : 해당 이미지의 높이 조절
```C
<img src="../assets/image/dog1.jpg" alt="강아지1">
```
### 1.7_테이블
   *	table : 표의 범위를 설정하는 태그
   *	tr : table row, 표에 한 줄을 추가하는 태그
   *	h : table header, 해당 줄에 제목 칸을 추가하는 태그(이때 글씨는 자동 굵어지고 가운데정렬로 됨)
   *	colspan 속성 : 열(가로)를 합치는 속성
   *	td : table data, 해당 줄에 데이터 칸을 추가하는 태그
   *	rowspan 속성 : row(행, 세로)를 합치는 속성
### 1.8_목록
   *	ul : unordered list : 순서 없는 리스트
   *	li : list item
   *	ol : ordered list : 순서 있는 리스트
   *	dl : 설명이 있는 리스트(dd : 들여쓰기 기능, dt : 설명할 텍스트)
### 1.9_입력
#### INPUT태그를 이용해 사용자로부터 다양한 입력을 받을 수 있다.
   *	Text : 일반적인 텍스트를 입력받는 칸
   *	Password : 텍스트를 가려주는 입력칸
   *	Radio : 여러가지 중 하나만 선택할 수 있는 버튼(이때 name 속성으로 카테고리를 지정해줘야 함 또한 label 속성을 통해 텍스트를 클릭해도 해당 개체가 클릭할 수 있게 할 수 있음)
   *	Checkbox : 여러가지 항목 중 여러 개를 선택할 수 있는 버튼
   *	Date : 날짜를 입력받는 칸
   *	Email : 이메일을 입력받는 칸, 약간의 이메일 형식 검사를 해준다
   *	Color : 컬러를 입력할 수 있는 칸
   *	textarea : 아주 긴 내용의 텍스트를 입력할 수 있다
   *	select : 사용자가 여러 옵션 중 하나를 선택할 수 있다.(option 태그를 통해 옵션을 추가할 수 있음)
#### form 태그
 *	action태그 속성 : submit이 발생했을 시 데이텨를 전송할 URL
 *	method태그 속성 : GET/POST/PUT/PATCH… 등의 http 데이터 전송 방식 설정
# 2.CSS
### 2.1_CSS이란
   *	모든 HTML요소가 어떤 모습으로 보여야 할 지 정의해놓는 곳
   *	스타일시트를 작성할 때는 CSS라는 언어를 사용한다
   *	웹브라우저는 스타일시트를 보고 해당 요소의 디자인을 결정한다
### 2.2_선택자
   *	Selector(선택자) { property(속성) : value(값); property : value;…. : CSS의 형식
   *	CSS에서는 선택자를 이용해 원하는 요소를 선택할 수 있다.
   *	tag : 해당 태그인 모든 HTML요소를 선택한다
   *	.class : 해당 클래스 속성(attribute)을 가진 모든 HTML요소를 선택한다
   *	#id : 해당 ID 속성을 가진 모든 HTML요쇼를 선택한다
#### 선택자 우선순위
   *	태그<.class<#id
   *	같은 우선순위인 경우 가장 나중에 작성한 스타일이 적용된다
#### CSS Diner로 선택자 연습
<img width="800" alt="cssdiner" src="https://user-images.githubusercontent.com/82793713/124751493-a8198a80-df61-11eb-9982-95a35db15b6a.PNG"></img><br/>
### 2.3_CSS 적용
   *	Inline CSS (줄 내부 CSS)
   *	Internal CSS (페이지 내부 CSS)
   *	External CSS (페이지 외부 CSS)
#### External CSS(페이지 외부 CSS)적용 하는 법 
```C
<link rel="stylesheet" href="./css 파일이 있는 위치">
```
### 2.4_배경
   *	background-image : url(‘url 넣는 곳’)=>이미지가 바둑판 배열로 여러 개 나타남
   *	background-size : 이미지의 사이즈(cover로 하면 사이즈에 맞게 이미지 사이즈가 조절됨)
### 2.5_여백
#### Margin
   *	해당 요소의 border 바깥쪽의 여백
   *	해당 요소와 다른 요소와의 거리를 결정한다
   *	Top margin과 bottom margin이 만나는 곳에서는 둘 중 더 높은 margin만 적용된다
   *	Margin을 auto로 설정하면 자동으로 요소를 가운데로 정렬한다(좌우 margin만 되지 상하 margin은 되지 않으므로 따로 해줘야함)
#### Padding
   * Padding은 컨텐츠부터 border까지의 여백이다
### 2.6_단위
#### 절대 길이 단위
   *	px : 픽셀(화소)
   *	mm : 밀리미터
   *	cm : 센치미터
   *	in : 인치
#### 상대 길이 단위
*	em : 현재 요소의 font-size에 비례한 크기조절
*	rem : 현제 페이지 html태그에 설정된 font-size에 비례한 크기 조절
*	vw : viewport width. 현재 웹 페이지를 보고있는 프로그램의 너비에 기반
*	vh : viewport height. viewport의 높이에 기반한 크기 조절
### 2.7_텍스트
*	text-align : 텍스트 정렬
*	vertical align : 줄 내부에서의 위치 설정
*	text-decoration : 밑줄
*	text-transform : 대소문자 변경
*	text-indent : 들여쓰기
*	letter-spacing : 글자 간격 설정
*	word-spacing : 단어 간격 설정
*	line-height : 줄 간격 설정(-px은 안먹힘)
*	white-space : 자동 줄 바꿈 설정
### 2.8_글꼴
#### font-family
*	font-family 속성으로 원하는 글꼴을 선택할 수 있다
*	기본적으로 사용자에 컴퓨터에 설치되지 않은 글꼴을 사용할 수 없다
*	사용자의 컴퓨터에 해당 글꼴이 로드되지 않는 경우에 대비하여 여러 예비용 글꼴을 설정해놓을 수 있다
*	사용자에게 번거롭게 글꼴을 설치하게 하는것보다는 CDN을 많이 활용한다
```C
@import url('https://fonts.googleapis.com/css2?family=Nanum+Myeongjo&display=swap');
div1{
    font-family: 'Nanum Myeongjo', serif;
}
```
### 2.9_가상클래스
*	first-child, nth-child(n/even/odd), last-child=>요소가 부모의 특정 번째 요소일 때를 선택함
*	first-of-type, nth-if-type(n/even/odd), last-of-type)=>요소가 같은 타입들 중에서 특정 번째 요소일 때를 선택함
*	hover=>요소에 마우스가 올라가 있는 상황을 선택함
*	link=>해당 요소가 링크일때를 선택한다
*	active=>해당 링크가 마우스로 활성화되고 있는 상황을 선택한다
*	visited=>이미 방문했던 링크일 때를 선택한다
*	더 많은 가상 클래스를 알고 싶으면 구글에 css pseudo class를 검색!
### 2.10_디스플레이
*	해당 요소가 어떻게 보여야 할지를 결정하는 속성
*	이 속성의 기본값으로는 inline, block이 있다
#### inline 요소의 특징
*	문단 내부에서 영역을 지정할 때 사용한다
*	새 줄에서 시작하지 않고, 필요한 내용만큼의 영역을 차지한다
*	padding과 margin을 고려하지 않고 배치된다
```C
<a>
```
#### block 요소의 특징
*	항상 새 줄에서 시작한다
*	기본 너비는 100%여서 화면 끝까지 뻗어나간다
*	padding과 margin이 제대로 적용된다
*	박스취급
```C
<div>
```
### 2.11_display: flex
* justify-content=>Flex 요소들을 가로선 상에서 정렬
  * flex-start(기본값), flex-end, center, space-between, space-around, apace-evenly
* flex-direction=>정렬할 방향을 지정
  * row(기본값), row-reverse, column, column-reverse
* align-items=>Flex 요소를 세로선 상에서 정렬
  * flex-start, flex-end, center, baseline, stretch(기본값)
* align-self=>지정된 align-items 값을 무시하고 Flex 요소를 새로선 상에서 정렬
  * flex-start, flex-end, center, baseline, stretch(기본값)
* flex-flow=>flex-direction and flex-wrap
* align-content=>세로선 상에 여분의 공간이 있는 경우 Flex 컨테이너 사이의 간격을 조정
  * flex-start, flex-end, center, space-between, space-around, apace-evenly, stretch(기본값)
* flex-wrap=> Flex 요소들을 한 줄 또는 여러 줄에 걸쳐 정렬
  * nowrap(기본값), wrap, wrap-reverse
#### flexboxfroggy로 선택자 연습
<img width="960" alt="캡처" src="https://user-images.githubusercontent.com/82793713/124755652-97b7de80-df66-11eb-9c47-7c1dbf1eba56.PNG"></img><br/>
### 2.12_display: grid
* column과 row를 설정할 수 있는 레이아웃
* grid-template-columns을 통해 columns의 개수와 각 컬럼의 폭을 정할 수 있음
```C
grid-template-columns: 25% 25% 10% auto;
```
* grid-template-rows를 통해 row의 개수와 각 행의 높이를 정할 수 있음
```C
grid-template-rows: 25% 25% auto;
```
* column-gap, row-gap을 통해 각 요소의 garp을 줄 수가 있다
### 2.13_position property
*	요소의 위치를 마음대로 설정하기 위한 속성
*	position: static=>기본값. 포지션이 설정되지 않은 상태
*	position: absolute=>포지션이 static이 아닌 부모 요소를 기준으로 절대적인 위치를 설정(없다면 웹브라우저를 기준으로)
*	position: relative=>상대적인 위치를 설정
*	position은 모두 부모 요소를 기준으로 결정된다
*	position: fixed - viewport에서 항상 고정적인 위치를 설정
* position: sticky=>처음에는 원래 위치에 존재하다가 스크롤이 내려가면 고정될 위치를 설정
### 2.14_float
*	다른 내용들이 해당 요소를 비켜가게 만든다
*	float을 더 이상 적용하지 싶지 않은 경우 clear로 해제해줘야 한다
### 2.15_반응형 웹 사이트
*	viewport의 크기에 따라 스타일이 달라지는 웹 사이트
*	Media Query를 사용한다
* @medai 기기타입 and (원하는 크기)
#### Media Types
*	all : 모든 타입
*	print: 프린터기에서 볼 때의 타입
* screen: 컴퓨터 스크린, 테블릿, 스마트폰 등의 일반 기기
* speech: 화면을 읽어주는 기기