# 리스트 치환자

리스트 치환자는 카테고리, 검색, 태그의 글 리스트를 표시합니다.

## 리스트 그룹
- `<s_list>`: 리스트 그룹 치환자
	- `[##_list_conform_##]`: 카테고리 이름, 검색어, 태그명
	- `[##_list_count_##]`: 글의 총 개수

## 아이템 반복 그룹
- `<s_list_empty>`: 리스트에 글이 없는 경우 보이는 영역
- `<s_list_rep>`: 리스트 아이템이 반복되는 영역
	- `[##_list_rep_link_##]`: 글의 고유 주소
	- `[##_list_rep_regdate_##]`: 글이 작성된 날짜
	- `[##_list_rep_title_##]`: 글의 제목
	- `[##_list_rep_rp_cnt_##]`: 댓글 수
	- `[##_list_rep_author_##]`: 작성자 이름
  - `[##_list_rep_summary_##]`: 글 내용 요약
	- `<s_list_rep_thumbnail>`: 대표 이미지가 있는 경우 치환
    - `[##_list_rep_thumbnail_##]`: 대표 이미지

## 예
```html
<!-- 스킨 -->
<s_list>
	<div class="searchList">
		<h3>'[##_list_conform_##]'에 해당되는 글 [##_list_count_##]건</h3>
		<ol>
			<s_list_rep>
				<li>
					<span class="date">[##_list_rep_regdate_##]</span>
					<a href="[##_list_rep_link_##]">[##_list_rep_title_##]</a>
					<span class="cnt">[##_list_rep_rp_cnt_##]</span>
					<s_list_rep_thumbnail>
						<img src="[##_list_rep_thumbnail_##]">
					</s_list_rep_thumbnail>
				</li>
			</s_list_rep>
		</ol>
	</div>
</s_list>
```

```html
<!-- 변환 예 -->
<div class="searchList">
	<h3>'업데이트 소식'에 해당되는 글 2건</h3>
	<ol>
		<li>
			<span class="date">2016.01.25</span>
			<a href="/2289">1월 초대장이 배포되었습니다.</a>
			<span class="cnt">8</span>
			<img src="https://s1.daumcdn.net/cfile/tistory/1234">
		</li>
		<li>
			<span class="date">2015.12.22</span>
			<a href="/2283">12월 초대장이 배포되었습니다.</a>
			<span class="cnt">19</span>
			<img src="https://s1.daumcdn.net/cfile/tistory/5678">
		</li>
	</ol>
</div>
```
