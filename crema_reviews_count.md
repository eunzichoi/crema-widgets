# [크리마 간편리뷰] 리뷰 수 작업하기
메이크샵을 사용하는 업체
리뷰 수를 넣으려는 페이지에 ‘크리마 Init 스크립트’가 들어가있는지 먼저 확인합니다.

(!) 크리마 Init 스크립트란?
: 간편리뷰를 이용하기 위해서 필수적으로 넣어야 하는 스크립트입니다.

```
<!-- cre.ma / PC 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/reviews/init.js?domain=gaenso.com');</script>
```


위와 같은 코드가 크리마 Init 스크립트입니다.
 
```
<!-- cre.ma / Mobile 리뷰 초기화 / 스크립트를 수정할 경우 연락주세요 (support@cre.ma) -->
<script>(function(i,s,o,g,r,a,m){if(s.getElementById(g)){return};a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.id=g;a.async=1;a.src=r;m.parentNode.insertBefore(a,m)})(window,document,'script','crema-jssdk','//widgets.cre.ma/mobile/reviews/init.js?domain=gaenso.com');</script>
```