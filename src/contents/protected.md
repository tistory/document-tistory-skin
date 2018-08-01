# 보호글 치환자

- `<s_article_protected>`: 보호글 그룹치환자
  - `[##_article_rep_link_##]`: 보호글의 고유 주소
  - `[##_article_rep_title_##]`: 보호글의 제목
  - `[##_article_rep_category_link_##]`: 카테고리 링크
  - `[##_article_rep_category_##]`: 카테고리 명
  - `[##_article_rep_date_##]`: 글쓴 날짜
  - `[##_article_password_##]`: 보호글의 비밀번호 텍스트 박스의 Id값(label 사용 용도)
  - `[##_article_dissolve_##]`: 보호글의 비밀번호를 입력하고 엔터키나 확인버튼을 눌렀을 때 실행될 자바스크립트 코드가 들어갑니다.
  - `[##_article_rep_author_##]`: 작성자 이름 (*팀블로그용 치환자)

```html
<s_article_protected>
  <div class="entryProtected">
    <h2><a href="[##_article_rep_link_##]">[##_article_rep_title_##]</a></h2>
    <span class="date">[##_article_rep_date_##]</span>
    <p>보호되어 있는 글입니다. 내용을 보시려면 비밀번호를 입력하세요.</p>
    <p>
      <label for="[##_article_password_##]">비밀번호 ::</label>
      <input type="password" maxlength="16" id="[##_article_password_##]" name="[##_article_password_##]" value="" onkeydown="if (event.keyCode == 13)[##_article_dissolve_##]" />
      <input type="button" class="submit" value="submit" onclick="[##_article_dissolve_##]" />
    </p>
  </div>
</s_article_protected>
```
