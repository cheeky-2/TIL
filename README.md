# TIL
## Vs code 주요 단축키
* `Ctrl + K` -> `Ctrl + \` 위/아래 수직 화면 분할
* `Ctrl + \` 좌/우 수평 화면 분할
* `Ctrl + J` 터미널 실행/닫기
* `Q` or `Ctrl + C` 터미널 입력안되는 에러 해결
## 작업폴더 설명
* `html_basic/` : html기초 연습파일 모음
* `task/` : 과제제출 폴더, 파일 모음(폴더명은 날짜별로 구성됨)
* `README.md` : 배운 내용 기록, 어려운 점 및 막힌 점 자유롭게 기록
### 2025/04/04 - HTML 3일차 문서와 레이아웃
* `h1~h2`, `p`, `br`, `strong`, `em`, `del`, `s`, `sup`, `sub`
### 2025/04/07 - HTML 4일차 레이아웃
* `div`, `span`
* 웹/앱 레이아웃 방향과 의미에 따라 2개 이상의 요소를 묶어주는 레이아웃 요소
* `div`는 생성 시 반드시 그룹을 구분할 수 있는 이름을 설정해야 한다. `span`은 선택!
* 이름 작성 시 주의사항 : 반드시 용도에 맞는 의미있는 영단어 사용!!
### HTML 구조 공부 순서
1. 클론 코딩 & 클론 디자인할 사이트 정하기
2. 피그마에서 와이어프레임 만들기 (레이어, 폴더 이름 주의)
3. 피그잼에 일부 화면 넘겨서 태그 계획하기
4. 계획한 태그를 가족관계에 맞게 트리구조 만들기
5. Vs code에서 실제 HTML 작성하기 (트리구조 순서에 맞게 바깥쪽 -> 안쪽순서로!)
### 다른 환경에서 git 이어서 작업하기
1. 새폴더 연결하기
2. `git clone 저장소주소붙여넣기`
3. `cd 폴더이름`
4. 수정후 `git add .`으로 다시 업로드 준비
5. `git commit -m '변경사항 및 설명`
6. `git push origin main`으로 gitHub로 업로드
7. `git pull origin main`으로 학원에서 내려받기
-----
### 바로가기 메뉴 만들기
0. (조건) 화면이 수직으로 충분히 이동할 수 있을만큼 스크롤 준비
1. 바로가기 메뉴 a 태그 준비하기
2. 바로가기 위치 div id명 준비하기
3. 위 1번 `a` 속성 `href` 값으로 `#` 먼저 작성 후 위 2번 이름 작성하기
4. 위 3번 결과 예시) id가 abcd일 경우 `<a href="#abcd"></a>`
## a태그에서
* <a href="#"></a>
* 임시 링크 설정
* <a href="#main"></a>
* id main으로 바로가기 설정
* <a href="./basic/index.html"></a>
* 현재 위치 폴더에서 basic 폴더에 들어가서 index.html 열기
* <a href="./basic/index.html#main"></a>
* 현재 위치 폴더에서 basic 폴더에 들어가서 index.html 열고 그 안에 id main으로 바로가기
----
## CSS Style Sheet
* 외부스타일시트 파일 저장은 **styles**폴더에 `파일명.css` 저장한다.
* 위 파일 생성 후 CSS연결을 원하는 HTML파일 head위치에 `<link>`태그로 연결한다.
* HTML작성 후 HTML의 모든 디자인형태를 초기화하는 `reset.css` 반드시 연결!
* 웹글꼴(Noto Sans KR, Pretendard 등) 연결 시 HTML파일에 `<link>`태그 연결!
### head태그 내에 들어가는 link태그 작성 순서
1. 웹글꼴 포함 기타 플러그인 연결 주소
2. reset.css
3. 해당 HTML별 디자인.css
### 디자인 CSS 작성 시 작성 순서 및 주의사항
* **부모->자식**순서로 가장 바깥쪽 부모부터 먼저 선택자를 만들고 디자인한다.
* 레이아웃 관련 요소에 `width, height` 속성 작성 시 영역 확인을 위한 `background-color`를 꼭 함께 작성해서 정확히 구분한다. 이 때 색상은 쉬운 영역 구분을 위한 `aqua, lime, yellow, pink`등의 밝은 색상 위주로 사용한다. 영역 확인과 디자인 작업을 모두 마친 후 위 색상은 제거로 마무리해야한다.
* 실제 디자인에 들어가는 색상은 **rgba 또는 헥사코드**로 입력하고 테스트용으로 입력하는 임시 색상은 영문명으로 입력해야 한다.
### 자주 이용하는 CSS 속성 값과 기본값
* `letter-spacing` 자간  기본값:0  letter-spacing:-0.02em;
* `line-height` 행간  line-height:1.5;
* `font-size` 글자크기  font-size:1rem;
* `color` 글자색깔  color:#???;  or  rgba(?,?,?,0.?)
* `background-color` 배경색  background-color:#???;  or  rgba(?,?,?,0.?)
* `width` 가로크기  width:?px;
* `height` 세로크기  height:?px;
* `margin` 바깥쪽여백  margin:?px;
* `border-radius` 모서리둥글기  border-radius:?px;
* `font-weight` 글자굵기  기본값:400  font-weight:?;
* `font-family` 글꼴설정  font-family:'한글 또는 공백 포함 글꼴', 영어 글꼴, 대체 글꼴 유형;