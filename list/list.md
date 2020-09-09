# 리스트 치환자

리스트 치환자는 카테고리, 검색, 태그의 글 리스트를 표시합니다.

## 리스트 그룹
- `<s_list>`: 리스트 그룹 치환자
  - `[##_list_conform_##]`: 카테고리 이름, 검색어, 태그명
  - `[##_list_count_##]`: 글의 총 개수
  - `[##_list_description_##]`: 리스트 설명 (카테고리인 경우 카테고리 설명, 그외 블로그 설명)
  - `[##_list_style_##]`: 리스트 스타일 값 (class attribute로 활용 가능)
  - `<s_list_image>`: 리스트 대표 이미지가 있는 경우 동작
    - `[##_list_image_##]`: 리스트 대표 이미지 (카테고리인 경우 카테고리 대표이미지, 그외 블로그 대표이미지)

## 아이템 반복 그룹
- `<s_list_empty>`: 리스트에 글이 없는 경우 보이는 영역
- `<s_list_rep>`: 리스트 아이템이 반복되는 영역
  - `[##_list_rep_link_##]`: 글의 고유 주소
  - `[##_list_rep_regdate_##]`: 글 작성 날짜 (yyyy.mm.dd)
  - `[##_list_rep_date_year_##]`: 글 작성 세부시간 - 연도 (yyyy)
  - `[##_list_rep_date_month_##]`: 글 작성 세부시간 - 월 (mm)
  - `[##_list_rep_date_day_##]`: 글 작성 세부시간 - 일 (dd)
  - `[##_list_rep_date_hour_##]`: 글 작성 세부시간 - 시 (HH)
  - `[##_list_rep_date_minute_##]`: 글 작성 세부시간 - 분 (MM)
  - `[##_list_rep_date_second_##]`: 글 작성 세부시간 - 초 (SS)
  - `[##_list_rep_title_##]`: 글의 제목
  - `[##_list_rep_category_##]`: 글이 속한 카테고리 이름
  - `[##_list_rep_category_link_##]`: 글이 속한 카테고리 글 목록 url
  - `[##_list_rep_rp_cnt_##]`: 댓글 수
  - `[##_list_rep_author_##]`: 작성자 이름
  - `[##_list_rep_summary_##]`: 글 내용 요약
  - `[##_list_rep_thumbnail_url_##]`: 대표 이미지 원본 주소
  - `<s_list_rep_thumbnail>`: 대표 이미지가 있는 경우 치환
    - `[##_list_rep_thumbnail_##]`: 대표 이미지

## 리스트 스타일

리스트 스타일을 사용하기 위해서는 [스킨 정보 파일](common/index.xml.md)에 리스트 스타일 아이템을 정의해야 합니다. 리스트 스타일을 정의하면 카테고리 관리화면에서 리스트 스타일이 표시되고 사용자가 선택할 수 있습니다. 이를 사용하여 카테고리별로 다른 스타일을 적용할 때 사용할 수 있습니다.

```xml
<default>
    <liststyle>default liststyle 값</liststyle>
</default>
```

```xml
<liststyle>
  <item>
    <label>표시할 이름</label>
    <value>사용될 값</value>
  </item>
</liststyle>
```

## 사용 예

```html
<!-- 스킨 예 -->
<s_list>
  <div class="searchList [##_list_style_##]">
    <div <s_list_image>style="background-image:url('[##_list_image_##]')"</s_list_image>>
      <h3>'[##_list_conform_##]'에 해당되는 글 [##_list_count_##]건</h3>
      <p>[##_list_description_##]</p>
    </div>
    <ol>
      <s_list_rep>
        <li>
          <span class="date">[##_list_rep_regdate_##]</span>
          <a href="[##_list_rep_link_##]">[##_list_rep_title_##]</a>
          <span class="cnt">[##_list_rep_rp_cnt_##]</span>
          <s_list_rep_thumbnail>
            <img src="[##_list_rep_thumbnail_##]">
          </s_list_rep_thumbnail>
        </li>
      </s_list_rep>
    </ol>
  </div>
</s_list>
```

```html
<!-- 변환 예 -->
<div class="searchList grid">
  <div style="background-image:url('https://sample.com/image.jpg')">
    <h3>'업데이트 소식'에 해당되는 글 2건</h3>
    <p>새롭게 업데이트되는 내용을 알려드립니다.</p>
  </div>
  <ol>
    <li>
      <span class="date">2016.01.25</span>
      <a href="/2289">1월 초대장이 배포되었습니다.</a>
      <span class="cnt">8</span>
      <img src="https://s1.daumcdn.net/cfile/tistory/1234">
    </li>
    <li>
      <span class="date">2015.12.22</span>
      <a href="/2283">12월 초대장이 배포되었습니다.</a>
      <span class="cnt">19</span>
      <img src="https://s1.daumcdn.net/cfile/tistory/5678">
    </li>
  </ol>
</div>
```
