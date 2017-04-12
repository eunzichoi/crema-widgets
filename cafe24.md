# Cafe24 v3.0

## PC

### 로그인

레이아웃 (layout) > 기본 레이아웃 (basic) > 메인 레이아웃 (main.html 또는 header.html 또는 다른 경우도 있음. `@import`를 통해 공통으로 호출되는 파일을 찾으면 됨) > `module=Layout_stateLogon` 내부

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

<!-- cre.ma / PC 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/reviews/init.js?domain=geteatfood.com');</script>
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
})(window,document,'script','crema-jssdk','//widgets.cre.ma/reviews/init.js?domain=geteatfood.com');
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
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/reviews/init.js?domain=geteatfood.com');</script>
```

이전 리뷰에 `crema-hide` class 추가

### 내 게시글

마이쇼핑(myshop) > 나의 게시글 (board_list.html)

```html
<!-- cre.ma / PC 내 게시글 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-reviews" data-type="my-reviews"></div>

<!-- cre.ma / PC 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/reviews/init.js?domain=geteatfood.com');</script>
```

### 주문 내역

마이쇼핑(myshop) > 나의 주문내역 (order) > 주문내역 (list.html)

```html
<!-- cre.ma / PC 주문 리뷰 작성 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
 crema-new-review-link" data-cafe24-product-link="{$param_postscript}"

<!-- cre.ma / PC 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/reviews/init.js?domain=geteatfood.com');</script>
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
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/mobile/reviews/init.js?domain=geteatfood.com');</script>
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
})(window,document,'script','crema-jssdk','//widgets.cre.ma/mobile/reviews/init.js?domain=geteatfood.com');
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
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/mobile/reviews/init.js?domain=geteatfood.com');</script>
```

### 내 게시글

마이쇼핑(myshop) > 나의 게시글 (board_list.html)

```html
<!-- cre.ma / Mobile 내 게시글 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-reviews" data-type="my-reviews"></div>

<!-- cre.ma / Mobile 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/mobile/reviews/init.js?domain=geteatfood.com');</script>
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
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/mobile/reviews/init.js?domain=geteatfood.com');</script>
```

구매후기가 "첫번째 주문"과 "두번째 이후 주문" 두 군데 있으니 모두 반영해야합니다.
