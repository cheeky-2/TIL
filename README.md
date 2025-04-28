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
## 위치속성 float
* 블록, 인라인 요소를 좌(left), 우(right) 사용하는 위치 속성
* 좌/우 배치하고 싶은 요소가 형제인 경우 사용
* 형제가 3개 이상인 경우 1->2 옆으로 두고 3을 내리고 싶은 경우, 형제3에게 `clear:both`를 선언하여 이전형제의 float 정렬 제거하기
### 오른쪽으로 보내고 싶은 형제 요소가 2개 이상이라면?
* 2개를 묶어서 그룹으로 처리하고 `float:right` 한번만 작성한다.
* `float:right`는 2번 이상 사용하면 역순이 되므로 **한번만 작성해야한다!!**
### float를 적용하는 형제의 부모의 높이가 max-content(기본값)이라면?
* 부모의 높이를 제대로 인식못하므로 높이를 강제(px)시키거나 `overflow:hidden` 높이를 안주고 영역 재인식을 시켜 float에 의한 오류를 제거해야 한다.
## form 태그 관련 속성 주요 뜻과 사용 용도
* 입력 양식 `input type=` text, password, email, search, number 등...
* 선택 양식 `input type=` checkbox, radio, select, option 등...
* 입력 양식과 선택 양식에 따라 같은 스펠링 속성의 뜻이 달라지므로 주의해야 한다!
## 양식에 따라 다른 속성의 뜻
* `value` : 입력양식(사용자가 입력한 값(속성작성X)), 선택양식(사용자가 선택해서 서버에 전송되는 값(속성작성O))
* `name` : 입력양식(사용자가 선택해서 서버에 전송되는 값(작성O)), 선택양식(2개 이상(1개도 가능)의 선택양식을 묶어주는 동일 그룹(작성O))
* 입력양식에서 `value`의 초기값을 작성하는 경우 : 쇼핑몰의 주문수량(기본값 1)
## form 속성에 사용자정의값을 이름 작성할 경우 주의사항
* name, value, id, class 등 속성의 이름을 작성할 때는 **중복명칭_개별명칭**을 섞어서 작성한다.
* 중복명칭에서 주로 사용하는 단어 : `admin, user` 등
* 개별명칭은 요소의 특징에 따라 달라진다(`male, id, btn, pw등`)
* 중복명칭 설정 시 작성 방향도 동일하게 해야한다.
* `user_id == user_pw` O
* `user_id == pw_user` X
## 목록양식 select, option (선택 목록이 2개 이상일 경우)
* 기존목록비교해서 외우기 select(ul), option(li)
* `select`태그는 option을 묶어주는 그룹개념으로 그룹 속성(name)이 함께 적용된다.
* `option`태그는 사용자가 실제 선택하는 값이므로 데이터 구분값 속성(value) 작성한다.
* `option` 태그 작성 시 모든 value속성은 필수가 아닌 사용자가 선택하는 데이터에만 사용한다.
* 선택option -> 1. 컬러(x) 2. 블랙(black) 3. 화이트(white) 4. 코랄(coral)
## 선택양식 radio, checkbox 주의사항과 label 주의사항
* radio, checkbox는 name(동일 그룹), value(개별 데이터값) 속성을 구분해서 사용한다.
* `id`속성을 적용할때는 javascript와 연결을 위해서 하거나 또는 label의 `for` 속성 연결을 위해서 사용한다. 이때 id값은 기존 개별데이터값을 가진 `value`와 동일한 값을 작성해도 된다.
* `label`은 사용자가 선택하는 이미지 또는 글자를 묶어서 작성하고 기존 선택양식 input의 형제로 작성한다면 반드시 `for` 속성을 입력해서 input의 id와 동일하게 입력하고, 반대로 input의 부모로 작성한다면 for을 입력하지 않아도 된다. 대신 이 경우엔 선택하는 이미지 또는 글자를 반드시 다른 인라인 태그로 묶어야 한다.
* input radio, checkbox는 사용자커스텀CSS 디자인이 불가능하기 때문에 사이트에 어울리는 모습으로 디자인하고 싶다면 `display:none` 숨기고 선택글자를 묶은 태그에 `background-image`로  디자인 해야 한다.
### input과 label이 형제인 경우
* `<input id="a"><label for="a">선택글자</label>`
### input과 label이 부모-자식인 경우
* `<label><input id="a"><span>선택글자</span></label>`
## button 속성 종류와 사용처
* `<button type="속성종류" id="버튼구분명">보이는글자 or 이미지</button>`
* 속성종류 1. button : 범용기능(주소찾기, 중복확인, 이전, 다음, 재생, 정지 등)
* 속성종류 2. submit : `form action`주소에 `method`값 형태로 전달되는 최종 서버전송버튼
* 속성종류 3. reset : 취소 or 삭제 버튼(가입취소, 주문취소 등)
-----
## CSS Calc() 함수
* CSS에서 길이, 비율, 수치 등을 계산할 때 사용하는 함수
* 단위가 다른(px, % 등)값도 계산할 수 있어서 레이아웃 조정 시 유용함.
* `+, -, *, /` 산술 연산자 모두 사용 가능
* 계산시 **연산자 앞 뒤 반드시 공백 포함**해서 작성하기!!
### CSS Calc() 함수 예시
* `height:calc(50vh - 100px);`
* `padding:calc(100% - (10px * 3));` 우선순위 괄호 추가 사용 가능!
* `width:calc(90% - (60px + 5px));` 우선순위도 연산자 앞뒤 공백 필수!
* `width:calc(90% - 65px);`