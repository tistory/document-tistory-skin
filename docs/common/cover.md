# 커버

커버는 홈화면을 꾸미기 위해 제공되는 치환자입니다.

- `<s_cover_group>`: 커버 그룹 치환자
  - `<s_cover_rep>`: 개별 커버 표시
    - `<s_cover>`: 개별 커버. name 애트리뷰트로 이름을 지정한다. 정의되지 않은 이름의 커버는 사용되지 않는다.
      - `[##_cover_title_##]`: 개별 커버 타이틀
      - `[##_cover_url_##]`: 개별 커버 url
      - `<s_cover_item>`: 개별 커버 컨텐츠
        - `[##_cover_item_title_##]`: 컨텐츠 타이틀
        - `[##_cover_item_summary_##]`: 컨텐츠 요약/내용
        - `[##_cover_item_url_##]`: 컨텐츠 url
        - `<s_cover_item_thumbnail>`: 컨텐츠 이미지가 있는 경우에만 치환
          - `[##_cover_item_thumbnail_##]`: 컨텐츠 이미지
        - `<s_cover_item_article_info>`: 컨텐츠가 글인 경우에만 치환
          - `[##_cover_item_category_##]`: 카테고리 명
          - `[##_cover_item_category_url_##]`: 카테고리 url
          - `[##_cover_item_date_##]`: 발행시간
          - `[##_cover_item_comment_count_##]`: 댓글 수

### 커버 치환자 사용 예
```html
<s_cover_group>
  <s_cover_rep>
    <s_cover name='featured'>
      <div class='featured'>
        <s_cover_item>
          <div class='featured-item'>
            <s_cover_item_thumbnail>
              <img class="image" src="[##_cover_item_thumbnail_##]">
            </s_cover_item_thumbnail>
            <strong class="title">[##_cover_item_title_##]</strong>
            <a href="[##_cover_item_url_##]" class="action">자세히 보기</a>
          </div>
        </s_cover_item>
        <button class='btn-prev'>&lt;</button>
        <button class='btn-next'>&gt;</button>
      </div>
    </s_cover>
    
    <s_cover name='list'>
      <div id="mArticle" class="article_skin">
        <s_cover_item>
          <div class="list_content">
            <s_cover_item_thumbnail>
              <a href="[##_cover_item_url_##]" class="thumbnail_post"><img src="//i1.daumcdn.net/thumb/C148x148/?fname=[##_cover_item_thumbnail_##]"></a>
            </s_cover_item_thumbnail>
            <a href="[##_cover_item_url_##]" class="link_post">
              <strong class="tit_post">[##_cover_item_title_##]</strong>
              <p class="txt_post">[##_cover_item_summary_##]</p>
            </a>
            <s_cover_item_article_info>
              <div class="detail_info">
                <a href="[##_cover_item_category_url_##]" class="link_cate">[##_cover_item_category_##]</a>
                <span class="txt_bar"></span>
                [##_cover_item_date_##]
              </div>
            </s_cover_item_article_info>
          </div>
        </s_cover_item>
        
        <s_cover_url>
          <a class="btn-more" href="[##_cover_url_##]">더보기</a>
        </s_cover_url>
      </div>
    </s_cover>
  </s_cover_rep>
</s_cover_group>
```

## 커버 정의 (index.xml)

```xml
<cover>
  <item>
    <name>커버 아이템 이름</name>
    <label>사용자에게 표시할 이름</label>
    <description>설명</description>
  </item>
</cover>
```

### 커버 정의 예
```xml
<cover>
  <item>
    <name>featured</name>
    <label>Featured Posts</label>
    <description>화면 가득 표시되는 형태</description>
  </item>
  <item>
    <name>list</name>
    <label>Posts List</label>
    <description>이미지와 제목, 용약이 나열되는 형태</description>
  </item>
</cover>
```
