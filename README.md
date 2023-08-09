# 부트스트랩

# 컴포넌트

> 사용자가 사용하는 시스템에 대한 조작장치

> 독립된 기능의 모듈

### alerts

경고 메세지 창

class="alert alert-색상"

주로

```
붉은색 - 문제

파란색, 초록색 - 확인, 잘됨
```

경고창에 링크들어갈때

```
    <div class="alert alert-primary">
      This is an alert <a href="#" class="alert-link">link.</a>
    </div>
```

경고박스 ( 제목 + 내용 )

```
<div class="alert alert-danger">
<h4 class="alert-heading">제목</h4>
<p>내용</p>
</div>
```

아이콘

창 없애기

class="btn-close" : 버튼이 x로 나옴

data-bs-dismiss="alert" : alert 를 닫음

---

### 버튼

기본버튼

class="btn" 은 투명 버튼

class="btn btn-primary"

마우스올리면 색변화 버튼

class="btn btn-outline-primary"

버튼 사이즈

class="btn btn-primary btn-lg"

lg 기본 sm

블록버튼

d-grid 안에 있는 버튼

```
class="d-grid"
    class="btn btn-primary"
```

버튼그룹 : 버튼들을 모아서 부모가 버튼그룹이됨

버튼이 한 그룹으로 묶임

class="btn-group"

버튼그룹 사이즈

lg 기본 sm

세로방향 그룹 버튼

class="btn-group-vertical"

---

### 어코디언

어코디언 클래스안에 어코디언 아이템이 들어 있음

버튼 부분

내용 부분

show : 처음에 보여줌

```
data-bs-target="#collapseOne"

id="collapseOne"
```

collapse 합쳐서 없앤다!

버튼의 타겟과 내용의 id가 같아야 열리고 닫힘

```
class="accordion"   id="accordionParent"

  class="accordion-item"
    질문)class="accordion-header"
    질문)class="accordion-button"
          data-bs-target="#collapseOne"
          data-bs-toggle="collapse"
	...
    답변)class="accordion-collapse collapse"
          id="collapseOne"
          data-bs-parent="#accordionParent"
    답변)class="accordion-body"
```

---

### 캐로셀

> 캐러셀은 이미지나 텍스트의 슬라이드를 가로로 슬라이드시켜 여러 개를 표시하는 컴포넌트

```
캐로셀 id="carouselExample"  class="carousel slide" data-bs-ride="carousel"(auto)

 캐로셀이너 class="carousel-inner"

   이미지 넣어주기class="carousel-item active"
		img태그

```

> 오토플레잉 (마우스올리면 멈춤)

data-bs-ride="carousel"

> 독립 .carousel-item 지연 시간

data-bs-interval="1000" (1초)

> 사진 크기 맞추기

클래스에 c-img 를 추가 후 따로 스타일 설정

```
<style>
        height: 100%;
        object-fit: cover;
</style>
```

좌우컨트롤 버튼

타켓과 id가 같아야함

```
      <button
        class="carousel-control-prev"
        type="button"
        data-bs-target="#carouselExample"
        data-bs-slide="prev"
      >

        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">이전</span>
      </button>
```

인디케이터

타켓과 id가 같아야함

```
  <div class="carousel-indicators">
    <button type="button" data-bs-target="#carouselExample" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1">
    </button>
    <button type="button" data-bs-target="#carouselExample" data-bs-slide-to="1" aria-label="Slide 2">
    </button>
    <button type="button" data-bs-target="#carouselExample" data-bs-slide-to="2" aria-label="Slide 3">
    </button>
  </div>
```

> 캡션(설명문)

.carousel-caption

```
          <div class="carousel-caption d-none d-md-block">
            <h5 class="display-1">캡션제목</h5>
            <p>캡션내용</p>
          </div>
```

---

### 카드

class="card" 안에 이미지, 제목, 내용 넣을 수 있음

카드 width 기본값은 100%

```
class="card-body"

    class="card-title"(제목)

      class="card-text"(내용)
```

오버레이 이미지 : 이미지 안에 글자가 들어감

class="card-img-overlay"

> 카드 안에 링크, 리스트도 넣을 수 있음!

카드의 헤더와 푸터

class="card-header"

class="card-footer"

---

### 모달

> 모달창은 기본적으로 숨겨져있음

버튼의 타겟과 모달의 id 가 동일 해야함

타켓에 해당하는 모달이 열림

```
      <button
        class="btn btn-danger"
        data-bs-target="#ourModal"
        data-bs-toggle="modal"
      >
```

```
class="modal fade" id="ourModal" data-bs-backdrop="static"
```

모달닫는 X버튼

```
<button class="btn-close" data-bs-dismiss="modal"></button>
```

하단의 닫기버튼

```
  <button class="btn btn-primary" data-bs-dismiss="modal">
  닫기
  </button>
```

---

### 스피너 : 로딩

- spinner-border

class="spinner-border text-primary"

- spinner-grow

class="spinner-grow text-primary"

사이즈

spinner-grow-sm

사용예시

```
      <button class="btn btn-primary">
        <div class="spinner-grow spinner-grow-sm"></div>
        Loading...
      </button>
```

---

### 네브바

> 내비게이션 바는 .navbar를 .navbar-expand{-sm|-md|-lg|-xl|-xxl}로 감싸야 함

class="navbar navbar-expand-sm bg-body-tertiary"

화면이 sm사이즈가 되면 줄어듬

> 색상 설정 방법

```
class="navbar bg-primary border-bottom border-body" data-bs-theme="dark"
```

```
class="navbar bg-primary" data-bs-theme="dark"
```

```
class="navbar" style="background-color: #e3f2fd;"
```

> 여백이 없음

class="container-fluid"

> 네비게이션의 제목

class="navbar-brand"

> 햄버거 버튼(사이즈가 작아지면 나옴)

```
   <button
    class="navbar-toggler"
    type="button"
   data-bs-toggle="collapse"
   data-bs-target="#navbarNav"
   aria-controls="navbarNav"
   aria-expanded="false"
   aria-label="Toggle navigation"
    >
  <span class="navbar-toggler-icon"></span>
  </button>
```

> 메뉴 박스 (작아지면 없어짐)

class="collapse navbar-collapse" id="navbarNav"

> 메뉴 리스트

```
          <ul class="navbar-nav">
            <li class="nav-item">
              <a class="nav-link" href="#">로그인</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">가입하기</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Q&A</a>
            </li>
          </ul>
```

> 위치 변경

마진을 주면됨

리스트 앞쪽에 마진을 주면 ms-auto

---

### 페이지네이션

> 페이지 이동 및 표시

리스트로

> class="pagination"

> class="page-item disabled"

> class="page-item disabled" : 클릭이 안됨

> class="page-item active" : 현재 이 페이지에 있음

html 특수문자 형식 : &aaa;

가운데로 위치 justify-content-center

---

### 테이블

스트라이프 행
.table-striped

제목 서식변경
thead class="table-dark"

```
      <table class="table table-striped">
        <thead class="table-dark">
          <tr>
            <th scope="col">번호</th>
            <th scope="col">이름</th>
            <th scope="col">반</th>
            <th scope="col">이메일</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th scope="row">1</th>
            <td>마크</td>
            <td>햇님반</td>
            <td>mark@naver.com</td>
          </tr>
          <tr>
            <th scope="row">2</th>
            <td>제이콥</td>
            <td>햇님반</td>
            <td>jjcop@naver.com</td>
          </tr>
          <tr>
            <th scope="row">3</th>
            <td>펭수</td>
            <td>햇님반</td>
            <td>pengsu@naver.com</td>
          </tr>
        </tbody>
      </table>
```

---

### 브레드크럼

> CSS로 구분자를 자동으로 추가해 내비게이션 계층 내에서 현재 페이지의 위치를 표시

기본 class="breadcrumb"

슬래쉬(/)로 구분

AAA/BBB/CCC

커스텀

```
<nav style="--bs-breadcrumb-divider: '👉'">
```

a 태그의 언더바 없애고 싶을때

```
<style>
text-decoration: none;
</style>
```

---

### 프로그래스바

> 진행정도를 보여주는 바

class="progress"

안에

class="progress-bar"

프로그래스의 바 길이

style="width: 50%"

class="progress-bar w-100"

기본색은 파란색 색상은 백그라운드로

class="progress-bar bg-danger"

높이는 부모태그에

class="progress" style="height: 20px"

하나의 bar 안에 여러개 넣을 수 있음

```
      <div class="progress">
        <div class="progress-bar bg-primary" style="width: 15%">15%</div>
        <div class="progress-bar bg-success" style="width: 45%">45%</div>
        <div class="progress-bar bg-warning" style="width: 25%">25%</div>
      </div>
```

줄무늬 디자인 넣기

class="progress-bar progress-bar-striped bg-warning"

줄무늬 애니메이션 넣기

class="progress-bar progress-bar-striped progress-bar-animated"

<기본 컴포넌트 끝>
