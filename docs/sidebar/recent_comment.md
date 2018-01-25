# 최근 댓글

- `<s_rctrp_rep>`: 댓글을 반복 출력합니다
- `[##_rctrp_rep_link_##]`: 댓글로 이동할 주소
- `[##_rctrp_rep_desc_##]`: 댓글의 본문 일부
- `[##_rctrp_rep_name_##]`: 댓글을 쓴 사람 이름
- `[##_rctrp_rep_time_##]`: 댓글을 쓴 시간 

```html
<s_sidebar_element>
  <!-- 최근에 달린 댓글 -->
  <div class="recentComment">
    <h3>최근에 달린 댓글</h3>
    <ul id="recentComments">
      <s_rctrp_rep>
        <li>
          <a href="[##_rctrp_rep_link_##]">[##_rctrp_rep_desc_##].</a>
          <span class="info_wrap">
            <span class="name">[##_rctrp_rep_name_##]</span>
            <span class="date">[##_rctrp_rep_time_##]</span>
          </span>
        </li>
      </s_rctrp_rep>
    </ul>
  </div>
</s_sidebar_element>
```
