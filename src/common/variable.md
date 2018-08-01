# 스킨 옵션

- `<s_if_var_{VARIABLE_NAME}>`: 옵션의 값이 있으면 (bool 타입인 경우 true이면) 치환
- `<s_not_var_{VARIABLE_NAME}>`: 옵션의 값이 없으면 (bool 타입인 경우 false이면) 치환
- `[##_var_{VARIABLE_NAME}_##]`: 옵션의 값

```html
<style>
  .wrap_sub {
    background-image: url('[##_var_cover-image_##]');
  }
</style>

<s_var_if_scroll-load>
	<style>
		.article_skin .area_paging .inner_paging.scroll_spinner {
			width:48px; height:48px;
			background:url('./images/spinner.gif') no-repeat;
			height: 48px;
			width: 48px;
			margin: 0 auto;
		}
		.article_skin .area_paging .inner_paging.scroll_spinner * {
			display:none
		}
	</style>
	<script src="./images/scroll-load.js"></script>
</s_var_if_scroll-load>
```

## 옵션 정의 (index.xml)

```html
<variables>
  <variable>
    <name>치환자에서 사용할 이름</name>
    <label>사용자에게 표시할 이름</label>
    <description>설명 (optional)</description>
    <type>타입</type>
    <option>max, min, select option등 값을 설정하는데 사용되는 정보 (optional: SELECT타입의 경우 필수)</option>
    <default>설정하지 않은 경우 기본 값</default>
  </variable>
</variables>
```

### type
- STRING: 문자 입력
- SELECT: 옵션 선택 (옵션은 name, label, value 값을 가진 json객체로 정의)
  - option 예
  ```xml
    <option><![CDATA[
      [
        {"name":"light", "label":"밝은색", "value":"light"},
        {"name":"dark", "label":"어두운색", "value":"dark"}
      ]
    ]]></option>
  ```
- IMAGE: 이미지 url
- BOOL: true/false
- COLOR: 컬러값 (#000000)

### 옵션 정의 사용 예

```xml
<variables>
  <variable>
    <name>cover-image</name>
    <label>
      <![CDATA[ 커버이미지 ]]>
    </label>
    <type>IMAGE</type>
    <option />
    <default>
      <![CDATA[ https://t1.daumcdn.net/tistory/0/Ray2/images/header_default.jpg ]]>
    </default>
    <description>
      <![CDATA[ 커버 이미지를 변경합니다. ]]>
    </description>
  </variable>
  <variable>
    <name>scroll-load</name>
    <label>
      <![CDATA[ 무한스크롤 ]]>
    </label>
    <type>BOOL</type>
    <option />
    <default>true</default>
    <description>
      <![CDATA[ 글 리스트 끝에 다다르면 다음 페이지를 불러옵니다. ]]>
    </description>
  </variable>
  <variable>
    <name>point-color</name>
    <label>
      <![CDATA[ 대표 색 ]]>
    </label>
    <type>COLOR</type>
    <option />
    <default><![CDATA[#6bacce]]></default>
    <description>
      <![CDATA[대표 색을 사용합니다.]]>
    </description>
  </variable>
</variables>
```
