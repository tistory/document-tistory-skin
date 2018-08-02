# 공지사항 치환자

- `<s_notice_rep>`: 공지사항 그룹 치환자
  - `[##_notice_rep_link_##]` : '공지사항'에 등록된 글의 고유 주소
  - `[##_notice_rep_title_##]` : 글 제목
  - `[##_notice_rep_date_##]` : 글쓴 날짜
  - `[##_notice_rep_desc_##]` : 본문 내용
  - `[##_notice_rep_author_##]` : 작성자 이름 (*팀블로그용 치환자)

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
