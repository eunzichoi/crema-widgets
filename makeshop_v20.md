# Makeshop v2.0

## PC

### 로그인

상단 > 기본 상단

```html
<!--/if_login/-->
<!-- cre.ma / 로그인 회원 정보 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<i id="crema-login-name" style="display:none;"><!--/user_name/--></i>
<i id="crema-login-username" style="display:none;"><!--/user_id/--></i>
<!--/end_if/-->
```

### 메인

메인 > 메인

```html
<!-- cre.ma / 팝업을 띄우는 코드 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-popup"></div>

<!-- cre.ma / PC 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/reviews/init.js?domain=utg.kr');</script>
```

### 리뷰 목록

구매후기 (상품 리뷰) > 목록

```html
<!-- cre.ma / PC 리뷰 목록 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-reviews"></div>

<!-- cre.ma / 이전 리뷰 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-hide"></div>

<!-- cre.ma / PC 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/reviews/init.js?domain=utg.kr');</script>
```

이전 리뷰에 `crema-hide` class 추가

### 상품 리뷰

상품관련 > 상품 상세 페이지 > 기본 상세 페이지

```html
<!-- cre.ma / 상품 리뷰 평점 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-product-score" data-product-code="<!--/number/-->" data-target-id="crema-product-reviews"></div>

<!-- cre.ma / 상품 리뷰 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div id="crema-product-reviews" class="crema-product-reviews" data-product-code="<!--/number/-->"></div>

<!-- cre.ma / 팝업을 띄우는 코드 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-popup"></div>

<!-- cre.ma / PC 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/reviews/init.js?domain=utg.kr');</script>
```

### 포토 리뷰 목록

인사이드디자인I > 게시판 화면 관리

간편리뷰 -> 리뷰설정 -> 추가 리뷰 게시판 설정에서 게시판 추가 후 data-board-id에 게시판 ID 설정

```html
<!-- cre.ma / PC 포토리뷰 목록 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-reviews" data-board-id="1"></div>
<!-- data-no-auto-scroll="1"을 추가시 자동불러오기를 하지 않음 -->

<!-- cre.ma / 이전 리뷰 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-hide"></div>

<!-- cre.ma / PC 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/reviews/init.js?domain=utg.kr');</script>
```

이전 리뷰에 `crema-hide` class 추가

### 내 게시글

마이페이지 > 내 게시글 보기

```html
<!-- cre.ma / PC 내 게시글 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-reviews" data-type="my-reviews"></div>

<!-- cre.ma / PC 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/reviews/init.js?domain=utg.kr');</script>
```

### 주문 리뷰

주문관련 > 주문조회/후기 팝업 > 게시판 타입 후기 or 평점 타입 후기

```html

<!-- cre.ma / 로그인 회원 정보 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<i id="crema-login-name" style="display:none;"><!--/user_name/--></i>
<i id="crema-login-username" style="display:none;"><!--/user_id/--></i>

<!-- cre.ma / PC 주문 리뷰 작성 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<a href="<!--/review_list@link_write_open/-->" class="crema-new-review-link" data-makeshop-product-link="<!--/review_list@link/-->"><img src="/images/d3/modern_simple/btn/btn_h20_review_reg.gif" alt="후기작성" title="후기작성" /></a>


<!-- cre.ma / 이전 리뷰 작성 폼 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-hide"></div>

<!-- cre.ma / PC 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/reviews/init.js?domain=utg.kr');</script>
```

## Mobile - 모바일 D4 (개별디자인)

### 로그인

상단 > 기본 상단

```html
<!--/if_login/-->
<!-- cre.ma / 로그인 회원 정보 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<i id="crema-login-name" style="display:none;"><!--/user_name/--></i>
<i id="crema-login-username" style="display:none;"><!--/user_id/--></i>
<!--/end_if/-->
```

### 메인

메인 > 메인

```html
<!-- cre.ma / 팝업을 띄우는 코드 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-popup"></div>

<!-- cre.ma / Mobile 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/mobile/reviews/init.js?domain=utg.kr');</script>
```


### 리뷰 목록

게시판 디자인 > 구매후기 (상품 리뷰) > 목록

```html
<!-- cre.ma / 이전 리뷰 디폴트로 숨기기 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<style>
  .crema-hide {display: none;}
</style>

<!-- cre.ma / 리뷰 목록 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-reviews"></div>

<!-- cre.ma / 이전 리뷰 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-hide"></div>

<!--/if_link/-->
<!-- cre.ma / 상품 리뷰 이동 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-product-reviews-redirect" data-makeshop-product-link="<!--/link/-->"></div>
<!--/end_if/-->

<!-- cre.ma / 모바일 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/mobile/reviews/init.js?domain=utg.kr');</script>
```

### 포토 리뷰 목록

게시판 디자인 > 포토후기 > 목록

간편리뷰 -> 리뷰설정 -> 추가 리뷰 게시판 설정에서 게시판 추가 후 data-board-id에 게시판 ID 설정

```html
<!-- cre.ma / 포토 리뷰 목록 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-reviews" data-board-id="1"></div>
<!-- data-no-auto-scroll="1"을 추가시 자동불러오기를 하지 않음 -->

<!-- cre.ma / 이전 리뷰 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-hide"></div>

<!-- cre.ma / 모바일 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/mobile/reviews/init.js?domain=utg.kr');</script>
```

### 상품 리뷰

상품관련 > 상품 상세 페이지 > 기본 상세 페이지

```html
<!-- cre.ma / Mobile 상품 리뷰 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-product-reviews-link" data-product-code="<!--/number/-->">상품후기<span class="crema-product-reviews-count" data-product-code="<!--/number/-->"><!--/number/review_board_total_count/--></span></div>
<!-- data-hide-if-zero="1"을 추가시 리뷰개수가 0일 경우 숨김처리 -->

<!-- cre.ma / Mobile 상품 리뷰 쓰기 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<a class="crema-new-review-link" data-product-code="<!--/number/-->">상품리뷰쓰기</a>

<!-- cre.ma / 팝업을 띄우는 코드 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-popup"></div>

<!-- cre.ma / Mobile 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/mobile/reviews/init.js?domain=utg.kr');</script>
```

### 내 게시글

마이페이지 > 내 게시글 보기

```html
<!-- cre.ma / Mobile 내 게시글 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-reviews" data-type="my-reviews"></div>

<!-- cre.ma / Mobile 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/mobile/reviews/init.js?domain=utg.kr');</script>
```

### 주문 리뷰

마이페이지 > 주문 내역

```html
<!-- cre.ma / Mobile 주문 리뷰 작성 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<a href="<!--/order_list@product@review_write_link/-->" class="review crema-new-review-link" data-product-code="<!--/order_list@product@product_id/-->" data-review-source="mobile_my_orders"><span class="blue-btn box-round">리뷰</span></a>

<!-- cre.ma / Mobile 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/mobile/reviews/init.js?domain=utg.kr');</script>

<!-- cre.ma / Mobile 주문서 더보기 버튼 시 새로운 주소 호출 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>
$(window).load(function() {
  org_ajax = $.ajax;
  $.ajax = function(options) {
    var success = options.success;
    options.success = function(data, textStatus, jqXHR) {
      if(success)
        success(data, textStatus, jqXHR);
        new crema.MakeshopShopBuilder;
        c = new crema.NewReviewLinkWidget;
        c.attach();
    };
    return org_ajax(options);
  };
});
</script>
```

or

```html
<!-- cre.ma / Mobile 주문 리뷰 작성 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<!--/if_order_list@delivery@product@review_write_link/-->
<a href="<!--/order_list@delivery@product@review_write_link/-->" class="btn_write review crema-new-review-link" data-makeshop-product-link="<!--/order_list@delivery@product@review_write_link/-->" data-review-source="mobile_my_orders">리뷰작성</a>
<!--/end_if/-->

<!-- cre.ma / Mobile 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>
setTimeout(function(){
(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/mobile/reviews/init.js?domain=utg.kr');
},200);
</script>
```

### 리뷰 쓰기

구매후기 (상품 리뷰) > 수정/쓰기

```html
<!-- cre.ma / 모바일 리뷰 쓰기 Redirect / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-new-review-redirect" data-makeshop-product-link="<!--/link/-->"></div>

<!-- cre.ma / 모바일 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/mobile/reviews/init.js?domain=utg.kr');</script>
```

## Mobile - 파워팩

### 로그인

상단 > 기본 상단 > 디자인 추가(HTML 선택)

```html
<!-- cre.ma / 로그인 회원 정보 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<i id="crema-login-name" style="display:none;"><!--/user_name/--></i>
<i id="crema-login-username" style="display:none;"><!--/user_id/--></i>
```

### 메인

메인 > 메인 > 디자인 추가(HTML 선택)

```html
<!-- cre.ma / 팝업을 띄우는 코드 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-popup"></div>

<!-- cre.ma / Mobile 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/mobile/reviews/init.js?domain=utg.kr');</script>
```

### 리뷰 목록

게시판 디자인 > 구매후기 (상품 리뷰) > 목록 > 디자인 추가(HTML 선택)

```html
<!-- cre.ma / 리뷰 목록 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-reviews"></div>

<!-- hidden 시킬 노드 class을 찾아 넣어줌 -->
<!-- cre.ma / 모바일 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>
var element = document.getElementsByClassName("").first();
element.classList.add("crema-hide");

(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/mobile/reviews/init.js?domain=utg.kr');
</script>
```

### 상품 리뷰

상품관련 > 상품 상세 페이지 > 기본 상세 페이지 > 디자인 추가(HTML 선택)

```html
<!-- cre.ma / 팝업을 띄우는 코드 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-popup"></div>

<!-- cre.ma / Mobile 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>
var review_link = $(".bottom-menu a[href^='/m/review_list.html']");
var product_id = review_link.attr('href').match(/branduid=([0-9]{1,7})/)[1];
review_link.addClass("crema-product-reviews-link");
review_link.attr("data-product-code", product_id);

var product_reviews_count = review_link.siblings();
product_reviews_count.addClass("crema-product-reviews-count");
product_reviews_count.attr("data-product-code", product_id);

var product_reviews_link = $(".btn-center2 a[href^='/m/review_list']")
product_reviews_link.addClass("crema-product-reviews-link");
product_reviews_link.attr("data-product-code", product_id);

product_reviews_count = product_reviews_link.find("em");
product_reviews_count.addClass("crema-product-reviews-count");
product_reviews_count.attr("data-product-code", product_id);
product_reviews_count.attr("data-format", "({{count}})");

var em = $(".btn-center2 a[href^='/m/board'] em");
em.addClass("crema-hide");

(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/mobile/reviews/init.js?domain=utg.kr');
</script>
```

### 내 게시글

마이페이지 > 내 게시글 보기 > 디자인 추가(HTML 선택)

```html
<!-- cre.ma / 모바일 내 게시글 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<div class="crema-reviews" data-type="my-reviews"></div>

<!-- cre.ma / 모바일 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>
(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/mobile/reviews/init.js?domain=utg.kr');
</script>
```

### 주문 리뷰

마이페이지 > 주문 내역 > 디자인 추가(HTML 선택)

```html
<!-- review_links를 selector로 찾을 때 주의 깊게 확인 요망 -->
<!-- cre.ma / 모바일 리뷰 초기화 및 내 주문 리뷰 쓰기 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>
link_script = function() {
  var review_links = $(".mypage-order-list a[href^='/m/review_list.html']");
  review_links.each(function(){
    var $link = $(this);
    var product_id = $link.attr('href').match(/branduid=([0-9]{1,7})/)[1];
    $link.addClass("crema-new-review-link");
    $link.attr("data-review-source", "mobile_my_orders");
    $link.attr("data-product-code", product_id);
  });
};

org_ajax = $.ajax;
$.ajax = function(options) {
  var success = options.success;
  options.success = function(data, textStatus, jqXHR) {
    if(success)
      success(data, textStatus, jqXHR);
      $(".btn_review").hide();
      link_script();
      if(typeof crema == 'function') {
        c = new crema.NewReviewLinkWidget;
        c.attach();
      }
      $(".btn_review").show();
  };
  return org_ajax(options);
};

(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/mobile/reviews/init.js?domain=utg.kr');
</script>
```
