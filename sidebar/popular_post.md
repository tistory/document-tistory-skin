# 인기글

- `<s_rctps_popular_rep>`: 인기글을 반복 출력합니다
  - `[##_rctps_rep_link_##]`: 글 주소
  - `[##_rctps_rep_title_##]`: 글 제목
  - `[##_rctps_rep_rp_cnt_##]`: 글 댓글 갯수
  - `[##_rctps_rep_author_##]`: 작성자 이름 (*팀블로그용 치환자)
  - `[##_rctps_rep_date_##]`: 글 발행시간
  - `<s_rctps_rep_thumbnail>`: 대표 이미지가 있는 경우 치환
    - `[##_rctps_rep_thumbnail_##]`: 대표 이미지
  - `[##_rctps_rep_category_##]`: 카테고리 이름
  - `[##_rctps_rep_category_link_##]`: 카테고리 리스트 url

```html
<s_sidebar_element>
  <!-- 이 블로그 인기글 -->
  <div class="popularPost">
    <h3>이 블로그 인기글 </h3>
    <ul>
      <s_rctps_popular_rep>
        <li>
          <a href="[##_rctps_rep_link_##]">[##_rctps_rep_title_##]</a>
          <span class="cnt">[##_rctps_rep_rp_cnt_##]</span>
          <s_rctps_rep_thumbnail>
            <img src="[##_rctps_rep_thumbnail_##]"/>
          </s_rctps_rep_thumbnail>
          <a href="[##_rctps_rep_category_link_##]">[##_rctps_rep_category_##]</a>
        </li>
      </s_rctps_popular_rep>
    </ul>
  </div>
</s_sidebar_element>
```
