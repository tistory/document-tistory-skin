# 홈 커버

홈 커버는 홈화면을 꾸미기 위해 제공되는 치환자입니다.

- `<s_cover_group>`: 커버 그룹 치환자
  - `<s_cover_rep>`: 개별 커버 표시
    - `<s_cover>`: 개별 커버. name 애트리뷰트로 이름을 지정한다. 정의되지 않은 이름의 커버는 사용되지 않는다.
      - `[##_cover_title_##]`: 개별 커버 타이틀
      - `[##_cover_url_##]`: 개별 커버 url
      - `<s_cover_item>`: 개별 커버 컨텐츠
        - `<s_cover_item_not_article_info>`: 컨텐츠가 글이 아닌 경우에만 치환 (내부 치환자는 s_cover_item에 직접 사용 가능)
          - `[##_cover_item_title_##]`: 컨텐츠 타이틀
          - `[##_cover_item_summary_##]`: 컨텐츠 요약/내용
          - `[##_cover_item_url_##]`: 컨텐츠 url
          - `<s_cover_item_thumbnail>`: 컨텐츠 이미지가 있는 경우에만 치환
            - `[##_cover_item_thumbnail_##]`: 컨텐츠 이미지
        - `<s_cover_item_article_info>`: 컨텐츠가 글인 경우에만 치환
          - `[##_cover_item_title_##]`: 컨텐츠 타이틀
          - `[##_cover_item_summary_##]`: 컨텐츠 요약/내용
          - `[##_cover_item_url_##]`: 컨텐츠 url
          - `<s_cover_item_thumbnail>`: 컨텐츠 이미지가 있는 경우에만 치환
            - `[##_cover_item_thumbnail_##]`: 컨텐츠 이미지
          - `[##_cover_item_category_##]`: 카테고리 명
          - `[##_cover_item_category_url_##]`: 카테고리 url
          - `[##_cover_item_date_##]`: 발행날짜/시간 (yyyy.mm.dd HH:MM)
          - `[##_cover_item_simple_date_##]`: 발행날짜 (yyyy.mm.dd)
          - `[##_cover_item_comment_count_##]`: 댓글 수

### 치환자 사용 예
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
          <s_cover_item_article_info>
            <div class="list_content">
              <s_cover_item_thumbnail>
                <a href="[##_cover_item_url_##]" class="thumbnail_post"><img src="//i1.daumcdn.net/thumb/C148x148/?fname=[##_cover_item_thumbnail_##]"></a>
              </s_cover_item_thumbnail>
              <a href="[##_cover_item_url_##]" class="link_post">
                <strong class="tit_post">[##_cover_item_title_##]</strong>
                <p class="txt_post">[##_cover_item_summary_##]</p>
              </a>
              <div class="detail_info">
                <a href="[##_cover_item_category_url_##]" class="link_cate">[##_cover_item_category_##]</a>
                <span class="txt_bar"></span>
                [##_cover_item_date_##]
              </div>
            </div>
          </s_cover_item_article_info>

          <s_cover_item_not_article_info>
            <div class="list_content">
              <s_cover_item_thumbnail>
                <a href="[##_cover_item_url_##]" class="thumbnail_post"><img src="//i1.daumcdn.net/thumb/C148x148/?fname=[##_cover_item_thumbnail_##]"></a>
              </s_cover_item_thumbnail>
              <a href="[##_cover_item_url_##]" class="link_post">
                <strong class="tit_post">[##_cover_item_title_##]</strong>
                <p class="txt_post">[##_cover_item_summary_##]</p>
              </a>
            </div>
          </s_cover_item_not_article_info>
        </s_cover_item>
        
        <s_cover_url>
          <a class="btn-more" href="[##_cover_url_##]">더보기</a>
        </s_cover_url>
      </div>
    </s_cover>
  </s_cover_rep>
</s_cover_group>
```

## 정의 (index.xml)

커버를 사용하기 위해서는 [스킨 정보 파일](index.xml.md)에 커버 아이템을 정의해야 합니다.

```xml
<cover>
  <item>
    <name>커버 아이템 이름</name>
    <label>사용자에게 표시할 이름</label>
    <description>설명</description>
  </item>
</cover>
```

### 정의 예
```xml
<cover>
  <item>
    <name>featured</name>
    <label><![CDATA[Featured]]></label>
    <description><![CDATA[강조할 글을 표시합니다.]]></description>
  </item>
  <item>
    <name>list</name>
    <label><![CDATA[리스트]]></label>
    <description><![CDATA[글 리스트를 표시합니다.]]></description>
  </item>
</cover>
```

## 기본값

스킨 적용 즉시 제작자가 추천하는 홈커버가 적용되도록 하기 위해서 기본값을 사용할 수 있습니다. 스킨 정보 파일의 기본값에 JSON 값을 string으로 설정합니다.

```xml
<default>
  <cover>
    <![CDATA[ 홈 커버 기본값 ]]>
  </cover>
</default>
```

### 기본값 JSON 구조
```json
[
  {
    "name": "정의된 커버 아이템 name",
    "title": "커버 타이틀",
    "dataType": "내용의 데이터 타입",
    "data": "타입에 해당하는 데이터"
  },
  ...
]
```

- name: 정의된 커버 아이템으로 없는 커버를 사용할 경우 무시됩니다.
- title: 커버타이틀로 사용할 string 입니다.
- dataType: 내용유형으로 스킨 에디터에서 제공하는 유형 중 '최신 글', '직접 입력' 만 사용할 수 있습니다.
  - RECENT: 최신 글
  - CUSTOM: 직접 입력
- data: 커버 내용으로 유형별로 형태가 다릅니다.
  - RECENT: 카테고리와 개수를 설정할 수 있습니다.
    ```json
    {
      "category": "ALL",
      "size": 5
    }
    ```
    - category: 사용자의 카테고리를 알 수 없으므로 전체(ALL), 공지사항(NOTICE)만 사용할 수 있습니다.
    - size: 표시될 개수를 설정합니다. 1-100 까지 설정할 수 있습니다.
  - CUSTOM: 표시될 내용을 모두 설정
    ```json
    {
      "title": "컨텐츠 타이틀",
      "summary": "컨텐츠 타이틀",
      "url": "컨텐츠 요약/내용",
      "thumbnail": "컨텐츠 이미지"
    }
    ```

### 기본값 예
```json
[
  {
    "name": "featured",
    "title": "",
    "dataType": "CUSTOM",
    "data": [
      {
        "title": "첫번째 항목",
        "summary": "첫번째 항목의 summary",
        "url": "https://www.tistory.com",
        "thumbnail": "https://www.tistory.com/sample.png"
      },
      {
        "title": "두번째 항목",
        "summary": "두번째 항목의 summary",
        "url": "https://www.tistory.com",
        "thumbnail": "https://www.tistory.com/sample.png"
      }
    ]
  },
  {
    "name": "list",
    "title": "",
    "dataType": "LIST",
    "data": {
      "category": "ALL",
      "size": 5
    }
  }
]
```
