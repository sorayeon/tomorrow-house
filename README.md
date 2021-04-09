## 생각을 정리 합시다.

| Mobile | Tablet | Desktop | class           | class      |
|--------|--------|---------|-----------------|------------|
| O      | X      | X       | .mobile-only    | .sm-only   |
| X      | O      | X       | .tablet-only    | .md-only   |
| X      | X      | O       | .desktop-only   | .lg-only   |
| X      | O      | O       | .mobile-hidden  | .sm-hidden |
| O      | X      | O       | .tablet-hidden  | .md-hidden |
| O      | O      | X       | .desktop-hidden | .lg-hidden |

$md-breakpoint: 768px;

$lg-breakpoint: 1200px;

| Mobile  | Tablet     | Desktop |
|---------|------------|---------|
| 0 - 767 | 768 - 1199 | 1200 -  |

| class      | condition       | description                            |
|------------|-----------------|----------------------------------------|
| .sm-only   | min-width: 768  | 모바일만 보이는 조건 768 보다 크면 hide        |
| .md-only   | max-width: 767  | 태블릿만 보이는 조건 767 보다 작으면서          |
|            | min-width: 1200 | 태블릿만 보이는 조건 1200 보다 크면 hide       |
| .lg-only   | max-width: 1199 | 데스크탑만 보이는 조건 1199 보다 작으면 hide    |
| .sm-hidden | max-width: 767  | 모바일만 숨기는 조건 767 보다 작으면 hide      |
| .md-hidden | min-width: 768  | 태블릿만 보이는 조건 768 보다 크면서           |
|            | max-width: 1199 | 태블릿만 보이는 조건 1199 보다 작으면 hide     |
| .lg-hidden | min-width: 1200 | 데스크탑만 보이는 조건 1200 보다 크면 hide     |

# 내일의 집
### 1. GNB

* 로그인을 하지 않은 경우
```html
<div class="button-group">
  <button
    class="gnb-icon-button is-search lg-hidden"
    type="button"
    aria-label="검색창 열기 버튼"
  >
    <i class="ic-search"></i>
  </button>
  <a
    href="/"
    class="gnb-icon-button is-cart"
    aria-label="장바구니 페이지로 이동"
  >
    <i class="ic-cart"></i>
  </a>
  <div class="gnb-auth sm-hidden">
    <a href="/">로그인</a>
    <a href="/">회원가입</a>
  </div>
</div>
```


* 로그인을 했을 경우
```html
<div class="button-group">
  <button
    class="gnb-icon-button is-search lg-hidden"
    type="button"
    aria-label="검색창 열기 버튼"
  >
    <i class="ic-search"></i>
  </button>

  <a
    class="gnb-icon-button sm-hidden"
    href="/"
    aria-label="스크랩북 페이지로 이동"
  >
    <i class="ic-bookmark"></i>
  </a>

  <a
    class="gnb-icon-button sm-hidden"
    href="/"
    aria-label="내 소식 페이지로 이동"
  >
    <i class="ic-bell"></i>
  </a>

  <a
    href="/"
    class="gnb-icon-button is-cart"
    aria-label="장바구니 페이지로 이동"
  >
    <i class="ic-cart"></i>
    <strong class="badge">5</strong>
  </a>

  <button
    class="gnb-avatar-button sm-hidden"
    type="button"
    aria-label="마이메뉴 열기 버튼"
  >
    <div class="avatar-32">
      <img
        src="./assets/images/img-user-01.jpg"
        alt="사달러 아저씨"
      />
    </div>
  </button>
</div>
```