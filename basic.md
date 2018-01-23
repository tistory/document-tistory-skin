# 치환자 구조

티스토리의 치환자는 `그룹치환자`, `값치환자`의 2가지 형태를 가지고 있습니다. `그룹치환자`는 내부에 스킨 데이터를 포함하며 렌더링된 값으로 변환됩니다. `값치환자`는 해당하는 값으로 변환됩니다.

## 예
```html
<s_tag>
	<div class="taglog">
		<h3>태그</h3>
		<ul>
			<s_tag_rep>
				<li><a href="[##_tag_link_##]" class="[##_tag_class_##]">[##_tag_name_##]</a></li>
			</s_tag_rep>
		</ul>
	</div>
</s_tag>
```
- 그룹치환자: `<s_tag>`, `<s_tag_rep>`
- 값치환자: `[##_tag_link_##]`, `[##_tag_class_##]`, `[##_tag_name_##]`


## 그룹치환자

```html
<s_NAME>VALUE</s_NAME>
```

## 값치환자

```html
[##_NAME_##]
```
