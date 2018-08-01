# 검색

- `<s_search>`: 검색 입력폼을 출력할 영역입니다
  - `[##_search_name_##]`: 검색어 입력 박스 이름
  - `[##_search_text_##]`: 검색어
  - `[##_search_onclick_submit_##]`: 검색 온클릭 이벤트 

```html
<s_sidebar_element>
  <!-- 검색 -->
  <div class="search">
    <s_search>
      <input type="text" name="[##_search_name_##]" value="[##_search_text_##]" onkeypress="if (event.keyCode == 13) { [##_search_onclick_submit_##] }"
      />
      <input value="검색" type="button" onclick="[##_search_onclick_submit_##]" class="submit" />
    </s_search>
  </div>
</s_sidebar_element>
```
