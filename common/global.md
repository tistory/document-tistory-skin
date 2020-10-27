# 공통 치환자

## 스킨 치환자 그룹
- `<s_t3>`: 티스토리 공통 javascript 삽입 (필수)

```html
<!-- 치환 전 -->
<body>
  <s_t3>
  ...
  </s_t3>
</body>

<!-- 치환 후 -->
<body>
  <script type="text/javascript" src="https://t1.daumcdn.net/tistory_admin/blogs/script/blog/common.js"></script>
  <div style="margin:0; padding:0; border:none; background:none; float:none; clear:none; z-index:0"></div>

  ...
</body>
```

## 기본 정보

### 블로그 정보
- `[##_title_##]`: 블로그 제목
- `[##_image_##]`: 블로그 대표 이미지 url
- `[##_blog_image_##]`: 블로그 대표 이미지를 포함한 IMG 태그
- `[##_desc_##]`: 블로그 설명
- `[##_blogger_##]`: 블로그 소유자의 필명

### 블로그 URL
- `[##_blog_link_##]`: 블로그 url
- `[##_rss_url_##]`: rss feed 주소
- `[##_taglog_link_##]`: 태그로그 url
- `[##_guestbook_link_##]`: 방명록 url

### 기타
- `[##_page_title_##]`: 페이지 제목
- `[##_blog_menu_##]`: 블로그 메뉴 리스트
- `[##_body_id_##]`: 페이지 타입에 따른 id

| 페이지 타입 | body_id |
| --- | --- |
| 홈화면 | tt-body-index |
| 글화면 | tt-body-page |
| 카테고리 글 리스트 | tt-body-category |
| 보관함 글 리스트 | tt-body-archive |
| 태그 리스트 | tt-body-tag |
| 검색결과 리스트 | tt-body-search |
| 방명록 | tt-body-guestbook |
| 지역로그 | tt-body-location |


## 광고 치환자
- [##_revenue_list_upper_##] : 블로그 홈/목록 상단
- [##_revenue_list_lower_##] : 블로그 홈/목록 하단


## 사용 예
```html
<html>
<head>
  <title>[##_page_title_##]</title>
</head>
<body id='[##_body_id_##]'>
<s_t3>
  <header>
    <h1><a href="[##_blog_link_##]">[##_title_##]</a></h1>
    <!-- 블로그 홈/목록 상단 치환자 -->
    [##_revenue_list_upper_##]


    <!-- blog_menu사용 -->
    [##_blog_menu_##]

    <!-- 메뉴 직접 구성 -->
    <ul class="blogMenu">
      <li><a href="[##_rss_url_##]">RSS구독</a></li>
      <li><a href="[##_taglog_link_##]">태그</a></li>
      <li><a href="[##_guestbook_link_##]">방명록</a></li>
    </ul>    
  </header>

  <section class="sidebar"> 
    <!-- blog_image 사용 -->
    <div class="blogInfo">
      <div class="blogImage">[##_blog_image_##] </div>
      <div class="blogDesc">[##_desc_##] <span class="userID">[##_blogger_##]</span></div>
    </div>

    <!-- image 사용 -->
    <div class="blogInfo">
      <div class="blogImage"><img src="[##_image_##]"></div>
      <div class="blogDesc">[##_desc_##] <span class="userID">[##_blogger_##]</span></div>
    </div>
  </section>
    
    <!-- 블로그 홈/목록 하단 -->
    [##_revenue_list_lower_##]
</s_t3>
</body>
</html>
```
