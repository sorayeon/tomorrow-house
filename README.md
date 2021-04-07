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