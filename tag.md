# 태그 클라우드 치환자

태그 클라우드는 사용한 태그 리스트를 출력합니다.
- url : `/tag`

## 태그 영역
- `<s_tag>` : 태그 클라우드로 접근시 이 영역 내부의 치환자가 출력됩니다. 

## 태그 반복 영역
- `<s_tag_rep>` : 개별태그의 반복열입니다 
	- `[##_tag_link_##]` : 태그가 포함된 글을 출력하기 위한 URL 
	- `[##_tag_class_##]` : 총 5단계가 있는데 자주 사용한 순서로 `cloud1`-`cloud5`가 표시됩니다.
	- `[##_tag_name_##]` : 태그의 이름 

## 예
```html
<!-- 스킨 -->
<s_tag>
	<div class="taglog">
		<h3>태그</h3>
		<ul>
			<s_tag_rep>
			<li>
				<a href="[##_tag_link_##]" class="[##_tag_class_##]">[##_tag_name_##]</a>
			</li>
			</s_tag_rep>
		</ul>
	</div>
</s_tag>
```

```html
<!-- 변환 예 -->
<div class="taglog">
	<h3>태그</h3>
	<ul>
		<li>
			<a href="/tag/tistory" class="cloud1">tistory</a>
		</li>
		<li>
			<a href="/tag/kakao" class="cloud4">kakao</a>
		</li>
		<li>
			<a href="/tag/blog" class="cloud5">blog</a>
		</li>
	</ul>
</div>
```
