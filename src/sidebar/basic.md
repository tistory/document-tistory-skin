# 사이드바 구조

- `<s_sidebar>`: 사이드바 그룹치환자
  - `<s_sidebar_element>`: 사이드바 개별 엘리먼트 그룹치환자\
  첫번째 줄의 주석 `<!-- TITLE -->`은 사이드바의 타이틀로 사용됩니다.

```html
<div id="sidebar">
  <s_sidebar>
    <!-- 오른쪽 사이드바 -->
    <s_sidebar_element>
      <!-- 카테고리 -->
      ...
    </s_sidebar_element>
    <s_sidebar_element>
      <!--최근에 올라온 글 -->
      ...
    </s_sidebar_element>
    <s_sidebar_element>
      <!-- 카운터 -->
      ...
    </s_sidebar_element>
  </s_sidebar>

  <s_sidebar>
    <!-- 배너 삽입 사이드바 -->
    <s_sidebar_element>
      <!-- 배너 모듈 - 태터툴즈 -->
      ...
    </s_sidebar_element>
    <s_sidebar_element>
      <!-- 배너모듈 - 올린 -->
      ...
    </s_sidebar_element>
    <s_sidebar_element>
      <!-- 배너모듈 - RSS Feed -->
      ...
    </s_sidebar_element>
  </s_sidebar>
</div>
```
