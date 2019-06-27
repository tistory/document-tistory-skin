# 공지사항 치환자

- `<s_notice_rep>`: 공지사항 그룹 치환자
  - `[##_notice_rep_link_##]` : '공지사항'에 등록된 글의 고유 주소
  - `[##_notice_rep_title_##]` : 글 제목
  - `[##_notice_rep_date_##]`: 글 발행 날짜/시간 (yyyy.mm.dd HH:MM)
  - `[##_notice_rep_simple_date_##]`: 글 발행 날짜 (yyyy.mm.dd)
  - `[##_notice_rep_date_year_##]`: 글쓴 세부시간 - 연도 (yyyy)
  - `[##_notice_rep_date_month_##]`: 글쓴 세부시간 - 월 (mm)
  - `[##_notice_rep_date_day_##]`: 글쓴 세부시간 - 일 (dd)
  - `[##_notice_rep_date_hour_##]`: 글쓴 세부시간 - 시 (HH)
  - `[##_notice_rep_date_minute_##]`: 글쓴 세부시간 - 분 (MM)
  - `[##_notice_rep_date_second_##]`: 글쓴 세부시간 - 초 (SS)
  - `[##_notice_rep_desc_##]` : 본문 내용
  - `[##_notice_rep_author_##]` : 작성자 이름 (*팀블로그용 치환자)
  - `<s_notice_rep_thumbnail>`: 대표 이미지 썸네일이 표시되는 영역 (대표 이미지가 없는 경우 표시되지 않음)
    - `[##_notice_rep_thumbnail_url_##]`: 대표 이미지 썸네일 주소
    - `[##_notice_rep_thumbnail_raw_url_##]`: 대표 이미지 원본 주소

```html
<s_notice_rep>
  <div class="entryNotice">
    <div class="titleWrap">
      <h2><a href="[##_notice_rep_link_##]">[##_notice_rep_title_##]</a></h2>
      <span class="date"> [##_notice_rep_date_##]</span>
    </div>
    <div class="article">
      [##_notice_rep_desc_##]
    </div>
  </div>
</s_notice_rep>
```

## 퍼머링크 / 인덱스

퍼머링크 페이지에서와 인덱스 페이지에서 표시될 내용을 구분할 수 있습니다.\
(퍼머링크 페이지/인덱스 페이지 영역 밖에서 사용되는 치환자는 둘 모두에서 표시됩니다) 

### 퍼머링크
- `<s_permalink_article_rep>`: 퍼머링크 페이지일 때만 표시되는 영역입니다
(내부에서 사용하는 치환자는 `<s_article_rep>` 내부에서 사용하는 치환자와 동일합니다)

### 인덱스
- `<s_index_article_rep>`: 인덱스 페이지일 때만 표시되는 영역입니다
  - `[##_notice_rep_link_##]` : '공지사항'에 등록된 글의 고유 주소
  - `[##_notice_rep_title_##]` : 글 제목
  - `[##_notice_rep_date_##]`: 글 발행 날짜/시간 (yyyy.mm.dd HH:MM)
  - `[##_notice_rep_simple_date_##]`: 글 발행 날짜 (yyyy.mm.dd)
  - `[##_notice_rep_date_year_##]`: 글쓴 세부시간 - 연도 (yyyy)
  - `[##_notice_rep_date_month_##]`: 글쓴 세부시간 - 월 (mm)
  - `[##_notice_rep_date_day_##]`: 글쓴 세부시간 - 일 (dd)
  - `[##_notice_rep_date_hour_##]`: 글쓴 세부시간 - 시 (HH)
  - `[##_notice_rep_date_minute_##]`: 글쓴 세부시간 - 분 (MM)
  - `[##_notice_rep_date_second_##]`: 글쓴 세부시간 - 초 (SS)
  - `[##_notice_rep_desc_##]` : 본문 내용
  - `[##_notice_rep_author_##]` : 작성자 이름 (*팀블로그용 치환자)
  - `[##_notice_rep_summary_##]`: 글 내용 일부
  - `<s_notice_rep_thumbnail>`: 대표 이미지 썸네일이 표시되는 영역 (대표 이미지가 없는 경우 표시되지 않음)
    - `[##_notice_rep_thumbnail_url_##]`: 대표 이미지 썸네일 주소
    - `[##_notice_rep_thumbnail_raw_url_##]`: 대표 이미지 원본 주소

```html
<s_index_article_rep>
  <div class="list_content">
    <s_notice_rep_thumbnail>
      <img src="[##_notice_rep_thumbnail_url_##]">
    </s_notice_rep_thumbnail>

    <a href="[##_notice_rep_link_##]" class="link_post">
      <strong class="tit_post">[##_notice_rep_title_##]</strong>
      <p class="txt_post">[##_notice_rep_summary_##]</p>
    </a>

    <div class="detail_info">
      <a href="[##_notice_rep_category_link_##]" class="link_cate">
        [##_notice_rep_category_##]
      </a>
      <span class="txt_bar"></span>
      [##_notice_rep_date_##]
    </div>
  </div>
</s_index_article_rep>
```
