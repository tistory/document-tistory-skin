# 최근 글

- `<s_rctps_rep>`: 최근에 올라온 글을 반복 출력합니다
  - `[##_rctps_rep_link_##]`: 최근글로 이동할 주소
  - `[##_rctps_rep_title_##]`: 최근글의 제목
  - `[##_rctps_rep_rp_cnt_##]`: 최근글에 달린 댓글 갯수
  - `[##_rctps_rep_author_##]`: 작성자 이름 (*팀블로그용 치환자)

```html
<s_sidebar_element>
  <!-- 최근에 올라온 글 -->
  <div class="recentPost">
    <h3>최근에 올라온 글 </h3>
    <ul>
      <s_rctps_rep>
        <li>
          <a href="[##_rctps_rep_link_##]"> [##_rctps_rep_title_##].</a>
          <span class="cnt">[##_rctps_rep_rp_cnt_##]</span>
        </li>
      </s_rctps_rep>
    </ul>
  </div>
</s_sidebar_element>
```
