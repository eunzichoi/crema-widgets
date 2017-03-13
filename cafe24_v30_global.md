# Cafe24 v3.0 Global

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
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/reviews/init.js?domain=secretlabel.jp');</script>
```

### 리뷰 목록

게시판 (board) > 상품게시판 (product) > 상품사용후기 목록 (list.html)

```html
<!-- cre.ma / PC 리뷰 목록 & 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>
(function(i,s,o,g,r,a,m,board_no){
  if(s.getElementById(g)){return};
  m=location.href.match(/board[\/][^\/]*[\/](\d+)[\/]/),board_no=m?decodeURIComponent(m[1].replace(/\+/g, " ")):'';
  if(board_no == "4"){
    document.write("<div class='crema-reviews'></div>");
    a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m);
  }
})(window,document,'script','crema-jssdk','//widgets.cre.ma/reviews/init.js?domain=secretlabel.jp');
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
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/reviews/init.js?domain=secretlabel.jp');</script>
```

이전 리뷰에 `crema-hide` class 추가

### 내 게시글

마이쇼핑(myshop) > 나의 게시글 (board_list.html)

```html
<!-- cre.ma / PC 내 게시글 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-reviews" data-type="my-reviews"></div>

<!-- cre.ma / PC 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/reviews/init.js?domain=secretlabel.jp');</script>
```

### 주문 상세 내역

마이쇼핑(myshop) > 나의 주문내역 (order) > 주문상세내역 (detail.html)

```html
<!-- cre.ma / PC 주문 리뷰 작성 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<strong><a href="/board/product/write.html{$param_postscript}" class="crema-new-review-link" data-cafe24-product-link="{$param_postscript}">구매후기</a></strong>

<!-- cre.ma / PC 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/reviews/init.js?domain=secretlabel.jp');</script>
```

구매후기가 "첫번째 주문"과 "두번째 이후 주문" 두 군데 있으니 모두 반영해야합니다.

### 주문 내역

마이쇼핑(myshop) > 나의 주문내역 (order) > 주문상세내역 (list.html)

```html
<!-- cre.ma / PC 주문 리뷰 작성 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<a href="/board/product/write.html{$param_postscript}" class="{$postscript_display|display} crema-new-review-link" data-cafe24-product-link="{$param_postscript}"><img src="http://img.echosting.cafe24.com/design/skin/default/myshop/btn_order_comment2.gif" alt="구매후기" /></a>

<!-- cre.ma / PC 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/reviews/init.js?domain=secretlabel.jp');</script>
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
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/mobile/reviews/init.js?domain=secretlabel.jp');</script>
```


### 리뷰 목록

게시판 (board) > 상품게시판 (product) > 상품사용후기 목록 (list.html)

```html
<!-- cre.ma / Mobile 리뷰 목록 & 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>
(function(i,s,o,g,r,a,m,board_no){
  if(s.getElementById(g)){return};
  m=location.href.match(/board[\/][^\/]*[\/](\d+)[\/]/),board_no=m?decodeURIComponent(m[1].replace(/\+/g, " ")):'';
  if(board_no == "4"){
    document.write("<div class='crema-reviews'></div>");
    a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m);
  }
})(window,document,'script','crema-jssdk','//widgets.cre.ma/mobile/reviews/init.js?domain=secretlabel.jp');
</script>
```

이전 리뷰에 `crema-hide` class 추가

### 상품 리뷰

상품 (product) > 상품상세 (detail.html)

```html
<!-- cre.ma / Mobile 상품 리뷰 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<style>#prdReview .nodata {display: none;}</style>
<div class="crema-product-reviews-link" data-product-code="{$product_no}">상품후기<span class="crema-product-reviews-count" data-product-code="{$product_no}">0</span></div>
<!-- data-hide-if-zero="1"을 추가시 리뷰개수가 0일 경우 숨김처리 -->
```

or

```html
<!-- cre.ma / Mobile 상품 리뷰 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<p class="mRreview"><a href="/board/product/list.html?board_no=4&link_product_no={$product_no}" class="crema-product-reviews-link crema-product-reviews-count" data-product-code="{$product_no}" data-format="구매후기 ({{{count}}}건)">구매후기 ({$review_count}건)</a></p>
```

``` html
<!-- cre.ma / 팝업을 띄우는 코드 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-popup"></div>

<!-- cre.ma / Mobile 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/mobile/reviews/init.js?domain=secretlabel.jp');</script>
```

### 내 게시글

마이쇼핑(myshop) > 나의 게시글 (board_list.html)

```html
<!-- cre.ma / Mobile 내 게시글 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-reviews" data-type="my-reviews"></div>

<!-- cre.ma / Mobile 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/mobile/reviews/init.js?domain=secretlabel.jp');</script>
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
<strong><a href="/board/product/write.html{$param_postscript}" class="crema-new-review-link" data-cafe24-product-link="{$param_postscript}" data-review-source="mobile_my_orders">구매후기</a></strong>

<!-- cre.ma / Mobile 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/mobile/reviews/init.js?domain=secretlabel.jp');</script>
```

구매후기가 "첫번째 주문"과 "두번째 이후 주문" 두 군데 있으니 모두 반영해야합니다.
