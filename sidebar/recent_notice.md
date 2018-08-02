# 최근 공지사항

- `<s_rct_notice>`: 공지사항 리스트를 출력할 영역입니다
  - `<s_rct_notice_rep>`: 공지사항 리스트를 반복 출력합니다
    - `[##_notice_rep_link_##]`: 공지사항의 고유 주소
    - `[##_notice_rep_title_##]`: 공지사항의 글 제목 

```html
<s_sidebar_element>
  <!-- 공지사항 -->
  <s_rct_notice>
    <div class="notice">
      <ul>
        <s_rct_notice_rep>
          <li>
            <a href="[##_notice_rep_link_##]">[##_notice_rep_title_##]</a>
          </li>
        </s_rct_notice_rep>
      </ul>
    </div>
  </s_rct_notice>
</s_sidebar_element>
```
