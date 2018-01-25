# 페이징

리스트, 글, 방명록에서 공통으로 사용하는 페이징 치환자

- `<s_paging>`: 페이지가 출력되는 영역입니다
  - `<s_paging_rep>`: 페이지가 반복 출력됩니다
    - `[##_prev_page_##]`: 이전 페이지 링크
    - `[##_paging_rep_link_##]`: 페이지 링크
    - `[##_paging_rep_link_num_##]`: 페이지 번호
    - `[##_next_page_##]`: 다음 페이지 링크 

```html
<s_paging>
  <div class="paging">
    <a [##_prev_page_##] class="[##_no_more_prev_##]">◀ PREV </a>
    <span class="numbox">
      <s_paging_rep>
        <a [##_paging_rep_link_##] class="num">[[##_paging_rep_link_num_##]]</a>
      </s_paging_rep>
    </span>
    <a [##_next_page_##] class="[##_no_more_next_##]">NEXT ▶</a>
  </div>
</s_paging>
```
