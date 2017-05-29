# Cafe24 v3.0

## PC

### 수정하는 파일

- 모든 페이지에서 공통적으로 참조하는 헤더 파일
- 메인 페이지
- 리뷰 게시판
- 상품 상세 페이지
- 마이페이지 > 내 게시글 관리
- 주문목록 페이지

PC 버전에서는 기본적으로 위 6개 파일을 수정합니다.

### 로그인

간편리뷰 기능을 사용하기 위해선 쇼핑몰에 로그인한 회원의 정보를 우리가 알아야 합니다.
그 정보를 가져오기 위해서 아래의 코드를 삽입합니다.
{$id}, {$name}은 카페24에서 사용하는 가상태그이며, 실제 보여지는 HTML에서는 로그인한 사용자 ID, 로그인한 사용자 이름으로 치환됩니다.
우리는 #crema-login-username과 #crema-login-name라는 보이지 않는 요소를 만들어 두고, 여 요소에 해당 태그를 이용해서 Body에 삽입하고 그걸 자바스크립트에서 파싱 & 활용합니다.
로그인 정보 소스가 들어가는 파일은 딱 정해져있지 않아서, 찾아가는 과정이 필요합니다. `모든 페이지에서 공통적으로 참조하는 헤더 파일`을 찾아야 합니다. 카페24의 기본 디자인에서는 `/layout/basic/main.html`과 `/layout/basic/layout.html`

```html
<!-- cre.ma / 로그인 회원 정보 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div module="Layout_stateLogon" style="display:none;">
  <i id="crema-login-username" style="display:none;">{$id}</i>
  <i id="crema-login-name" style="display:none;">{$name}</i>
</div>
```

위에서 module이라는 Attribute는 카페24에서 사용하는 템플릿 코드입니다.
특정 태그에 module이라는 Attribute를 지정해주면 해당 태그 자기자신을 포함해서 내부에 있는 Child 태그들이 Cafe24 가상태그를 사용할 수 있습니다.
위의 소스에서 module="Layout_stateLogon"가 의미하는 바는, "핑몰에서 로그인"


### 메인

쇼핑몰 메인 (index.html)

```html
<!-- cre.ma / 팝업을 띄우는 코드 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-popup"></div>

<!-- cre.ma / PC 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/reviews/init.js?domain=under-vi.com');</script>
```

### 리뷰 목록

게시판 (board) > 상품게시판 (product) > 상품사용후기 목록 (list.html)

```html
<!-- cre.ma / PC 리뷰 목록 & 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>
(function(i,s,o,g,r,a,m,board_no){
  if(s.getElementById(g)){return};
  m=new RegExp("[\\?&]board_no=([^&#]*)").exec(location.search),board_no=m?decodeURIComponent(m[1].replace(/\+/g, " ")):'';
  if(board_no == "4"){
    document.write("<div class='crema-reviews'></div>");
    a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m);
  }
})(window,document,'script','crema-jssdk','//widgets.cre.ma/reviews/init.js?domain=under-vi.com');
</script>
```

이전 리뷰에 `crema-hide` class 추가

### 상품 리뷰

상품 (product) > 상품상세 (detail.html)

```html
<!-- cre.ma / 상품 리뷰 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<style>#prdReview .nodata {display: none;}</style>
<div class="crema-product-reviews" data-product-code="{$product_no}"></div>

<!-- cre.ma / 팝업을 띄우는 코드 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-popup"></div>

<!-- cre.ma / PC 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/reviews/init.js?domain=under-vi.com');</script>
```

이전 리뷰에 `crema-hide` class 추가

### 내 게시글

마이쇼핑(myshop) > 나의 게시글 (board_list.html)

```html
<!-- cre.ma / PC 내 게시글 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-reviews" data-type="my-reviews"></div>

<!-- cre.ma / PC 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/reviews/init.js?domain=under-vi.com');</script>
```

### 주문 내역

마이쇼핑(myshop) > 나의 주문내역 (order) > 주문내역 (list.html)

```html
<!-- cre.ma / PC 주문 리뷰 작성 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
 crema-new-review-link" data-cafe24-product-link="{$param_postscript}"

<!-- cre.ma / PC 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/reviews/init.js?domain=under-vi.com');</script>
```

## Mobile

### 로그인

레이아웃 (layout) > 메인 레이아웃 (main.html 또는 sidebar.html 또는 다른 경우도 있음. `@import`를 통해 공통으로 호출되는 파일을 찾으면 됨) > `module=Layout_stateLogon` 내부

```html
<!-- cre.ma / 로그인 회원 정보 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div module="Layout_stateLogon" style="display:none;">
  <i id="crema-login-username" style="display:none;">{$id}</i>
  <i id="crema-login-name" style="display:none;">{$name}</i>
</div>
```

### 메인

쇼핑몰 메인 (index.html)

```html
<!-- cre.ma / 팝업을 띄우는 코드 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-popup"></div>

<!-- cre.ma / Mobile 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/mobile/reviews/init.js?domain=under-vi.com');</script>
```


### 리뷰 목록

게시판 (board) > 상품게시판 (product) > 상품사용후기 목록 (list.html)

```html
<!-- cre.ma / Mobile 리뷰 목록 & 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>
(function(i,s,o,g,r,a,m,board_no){
  if(s.getElementById(g)){return};
  m=new RegExp("[\\?&]board_no=([^&#]*)").exec(location.search),board_no=m?decodeURIComponent(m[1].replace(/\+/g, " ")):'';
  if(board_no == "4"){
    document.write("<div class='crema-reviews'></div>");
    a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m);
  }
})(window,document,'script','crema-jssdk','//widgets.cre.ma/mobile/reviews/init.js?domain=under-vi.com');
</script>
```

이전 리뷰에 `crema-hide` class 추가

### 상품 리뷰

상품 (product) > 상품상세 (detail.html)

```html
<!-- cre.ma / Mobile 상품 리뷰 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<style>#prdReview .nodata {display: none;}</style>
<div class="crema-product-reviews" data-product-code="{$product_no}"></div>
<!-- data-hide-if-zero="1"을 추가시 리뷰개수가 0일 경우 숨김처리 -->
```

```html
<!-- cre.ma / 팝업을 띄우는 코드 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-popup"></div>

<!-- cre.ma / Mobile 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/mobile/reviews/init.js?domain=under-vi.com');</script>
```

### 내 게시글

마이쇼핑(myshop) > 나의 게시글 (board_list.html)

```html
<!-- cre.ma / Mobile 내 게시글 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-reviews" data-type="my-reviews"></div>

<!-- cre.ma / Mobile 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/mobile/reviews/init.js?domain=under-vi.com');</script>
```

### 주문 상세 내역

마이쇼핑(myshop) > 나의 주문내역 (order) > 주문상품정보 (order_detail_more.html)

```html
<!-- cre.ma / 로그인 회원 정보 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div module="Layout_statelogon" style="display:none;">
    <i id="crema-login-username" style="display:none;">{$id}</i>
    <i id="crema-login-name" style="display:none;">{$name}</i>
</div>

<!-- cre.ma / Mobile 주문 리뷰 작성 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
 crema-new-review-link" data-cafe24-product-link="{$param_postscript}" data-review-source="mobile_my_orders"

<!-- cre.ma / Mobile 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/mobile/reviews/init.js?domain=under-vi.com');</script>
```

구매후기가 "첫번째 주문"과 "두번째 이후 주문" 두 군데 있으니 모두 반영해야합니다.
