# 글 치환자

## 글 정보
- `<s_article_rep>`: 글 그룹 치환자
  - `[##_article_rep_link_##]`: 블로그 글의 고유 주소
  - `[##_article_rep_title_##]`: 블로그 글의 제목
  - `[##_article_rep_category_link_##]`: 카테고리 링크
  - `[##_article_rep_category_##]`: 카테고리 명
  - `[##_article_rep_date_##]`: 글쓴 날짜
  - `[##_article_rep_author_##]`: 작성자 이름 (*팀블로그용 치환자)
  - `[##_article_rep_desc_##]`: 블로그 본문 내용

```html
<s_article_rep>
  <div class="titleWrap">
    <h2><a href="[##_article_rep_link_##]">[##_article_rep_title_##]</a></h2>
    <div class="category">
      <a href="[##_article_rep_category_link_##]">[##_article_rep_category_##]</a>
    </div>
    <div class="date">[##_article_rep_date_##]</div>
  </div>

  <div class="article">
    [##_article_rep_desc_##]
  </div>
</s_article_rep>
```

## 관리기능
- `<s_ad_div>` : 글 관리기능 그룹치환자 (관리 권한 있는 경우만 표시)
  - `[##_s_ad_m_link_##]`: 수정
  - `[##_s_ad_m_onclick_##]`: 수정 온클릭 이벤트
  - `[##_s_ad_s1_label_##]`: 글의 현재 상태
  - `[##_s_ad_s2_onclick_##]`: 상태 변경 온클릭 이벤트
  - `[##_s_ad_s2_label_##]`: 이후 상태
  - `[##_s_ad_t_onclick_##]`: 트랙백 온클릭 이벤트
  - `[##_s_ad_d_onclick_##]`: 삭제 온클릭 이벤트 

```html
  <s_ad_div>
    <div class="admin">
      <a href="[##_s_ad_m_link_##]">수정</a> :
      <a href="#" onclick="[##_s_ad_m_onclick_##]">수정(창으로)</a> |
      ([##_s_ad_s1_label_##])→<a href="#" onclick="[##_s_ad_s2_onclick_##]">[##_s_ad_s2_label_##]</a> |
      <a href="#" onclick="[##_s_ad_t_onclick_##]">관련글(트랙백)</a> |
      <a href="#" onclick="[##_s_ad_d_onclick_##]">삭제</a>
    </div>
  </s_ad_div>
```

## 태그

- `<s_tag_label>`: 글과 관련된 태그가 출력되는 영역입니다.
  - `[##_tag_label_rep_##]`: 태그 반복 출력 

```html
  <s_tag_label>
    <div class="tagTrail">
      <span class="tagText">TAG </span> [##_tag_label_rep_##]
    </div>
  </s_tag_label>
```

## 댓글 수

- `<s_rp_count>`: 댓글의 갯수를 출력하는 영역
  - `[##_article_rep_rp_link_##]`: 댓글을 열고 닫는 온클릭 이벤트
  - `[##_article_rep_rp_cnt_##]`: 답글 수 

```html
<div class="actionTrail">
  <a href="#rp" onclick="[##_article_rep_rp_link_##]">
    <s_rp_count>
      댓글 <span class="cnt">[##_article_rep_rp_cnt_##]</span>개가 달렸습니다.
    </s_rp_count>
  </a>
</div>
```

## 퍼머링크 / 인덱스

퍼머링크 페이지에서와 인덱스 페이지에서 표시될 내용을 구분할 수 있습니다.\
(퍼머링크 페이지/인덱스 페이지 영역 밖에서 사용되는 치환자는 둘 모두에서 표시됩니다) 

### 퍼머링크
- `<s_permalink_article_rep>`: 퍼머링크 페이지일 때만 표시되는 영역입니다
(내부에서 사용하는 치환자는 `<s_article_rep>` 내부에서 사용하는 치환자와 동일합니다)

### 인덱스
- `<s_index_article_rep>`: 인덱스 페이지일 때만 표시되는 영역입니다
  - `[##_article_rep_link_##]`: 블로그 글의 고유 주소
  - `[##_article_rep_title_##]`: 블로그 글의 제목
  - `[##_article_rep_category_link_##]`: 카테고리 주소
  - `[##_article_rep_category_##]`: 카테고리 이름
  - `[##_article_rep_date_##]`: 글쓴 날짜
  - `[##_article_rep_author_##]`: 작성자 이름
  - `[##_article_rep_summary_##]`: 글 내용 일부
  - `<s_article_rep_thumbnail>`: 대표 이미지 썸네일이 표시되는 영역입니다 (대표 이미지가 없는 경우 표시되지 않음)
    - `[##_article_rep_thumbnail_url_##]`: 대표 이미지 썸네일 주소
    - `[##_article_rep_thumbnail_raw_url_##]`: 대표 이미지 원본 주소

```html
<s_index_article_rep>
  <div class="list_content">
    <s_article_rep_thumbnail>
      <img src="[##_article_rep_thumbnail_url_##]">
    </s_article_rep_thumbnail>

    <a href="[##_article_rep_link_##]" class="link_post">
      <strong class="tit_post">[##_article_rep_title_##]</strong>
      <p class="txt_post">[##_article_rep_summary_##]</p>
    </a>

    <div class="detail_info">
      <a href="[##_article_rep_category_link_##]" class="link_cate">
        [##_article_rep_category_##]
      </a>
      <span class="txt_bar"></span>
      [##_article_rep_date_##]
    </div>
  </div>
</s_index_article_rep>
```

## 카테고리의 다른 글

글이 속한 카테고리의 다른 글을 보여줄 수 있습니다.\
카테고리에 속하지 않은 글에는 표시되지 않습니다. 

- `<s_article_related>`: 카테고리 글 더보기 영역
  - `[##_article_related_rep_type_##]`: 글의 type (대표이미지 없음: text_type, 대표이미지 있음: thumb_type)
  - `[##_article_related_rep_link_##]`: 글 주소
  - `[##_article_related_rep_title_##]`: 글 제목
  - `[##_article_related_rep_date_##]`: 글 작성시간
  - `<s_article_related_rep_thumbnail>`: 대표 이미지 썸네일이 표시되는 영역입니다 (대표 이미지가 없는 경우 표시되지 않음)
    - `[##_article_related_rep_thumbnail_link_##]`: 대표 이미지 썸네일 주소

```html
<s_article_related>
  <div class="area_related">
    <strong class="tit_related">'[##_article_rep_category_##]' Related Articles</strong>
    <ul class="list_related">
      <s_article_related_rep>
        <li class="[##_article_related_rep_type_##]">
          <a href="[##_article_related_rep_link_##]" class="link_related">
            <s_article_related_rep_thumbnail>
              <span class="thumb_related">
                <img src="[##_article_related_rep_thumbnail_link_##]" class="img_related" alt="">
              </span>
            </s_article_related_rep_thumbnail>
            <span class="txt_related">[##_article_related_rep_title_##]</span>
            <span class="date_related">[##_article_related_rep_date_##]</span>
            <span class="frame_related"></span>
          </a>
        </li>
      </s_article_related_rep>
    </ul>
    <a href="[##_article_rep_category_link_##]" class="link_more">more</a>
  </div>
</s_article_related>
```
