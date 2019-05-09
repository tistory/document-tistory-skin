# 공지사항 치환자

- `<s_page_rep>`: '페이지'가 출력되는 영역입니다.\
(스킨에 페이지치환자가 존재하지 않는 경우 글 치환자에 페이지가 표시됩니다.)
  - `[##_article_rep_link_##]`: 고유 주소
  - `[##_article_rep_title_##]`: 제목
  - `[##_article_rep_date_##]`: 글 발행 날짜/시간 (yyyy.mm.dd HH:MM)
  - `[##_article_rep_simple_date_##]`: 글 발행 날짜 (yyyy.mm.dd)
  - `[##_article_rep_desc_##]`: 본문 내용
  - `[##_article_rep_author_##]`: 작성자 이름 (*팀블로그용 치환자)

```html
<s_page_rep>
  <div>
    <h2><a href="[##_article_rep_link_##]">[##_article_rep_title_##]</a></h2>
    <div>
      [##_article_rep_desc_##]
    </div>
  </div>
</s_page_rep> 
```
