# 링크

- `<s_link_rep>`: 링크가 반복 출력됩니다
- `[##_link_url_##]`: 사이트로 이동할 주소
- `[##_link_site_##]`: 사이트 이름 

```html
<s_sidebar_element>
  <!-- 링크 -->
  <div class="link">
    <h3>링크</h3>
    <ul>
      <s_link_rep>
        <li>
          <a href="[##_link_url_##]" onclick="window.open(this.href); return false"> [##_link_site_##].</a>
        </li>
      </s_link_rep>
    </ul>
  </div>
</s_sidebar_element>
```
