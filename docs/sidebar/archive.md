# 글 보관함

- `<s_archive_rep>`: 월별 글 보관함을 출력합니다
- `[##_archive_rep_link_##]`: 각 월별 보관함으로 이동할 주소
- `[##_archive_rep_date_##]`: 년과 월을출력
- `[##_archive_rep_count_##]`: 각 월별에 속한 글의 갯수 

```html
<s_sidebar_element>
  <!-- 글 보관함 -->
  <div class="archive">
    <h3>글 보관함</h3>
    <ul>
      <s_archive_rep>
        <li>
          <a href="[##_archive_rep_link_##]">[##_archive_rep_date_##] </a>
          <span class="cnt">([##_archive_rep_count_##])</span>
        </li>
      </s_archive_rep>
    </ul>
  </div>
</s_sidebar_element>
```
