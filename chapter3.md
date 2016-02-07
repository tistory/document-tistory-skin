# 리스트 치환자

리스트 치환자는 카테고리, 검색, 태그의 글 리스트를 표시합니다.

## 리스트 영역
- `<s_list>`: 리스트 영역
	- `[##_list_conform_##]`: 카테고리 이름, 검색어, 태그명
	- `[##_list_count_##]`: 글의 총 개수

## 아이템 반복 영역
- `<s_list_rep>`: 리스트 아이템이 반복되는 영역
	- `[##_list_rep_link_##]`: 글의 고유 주소
	- `[##_list_rep_regdate_##]`: 글이 작성된 날짜
	- `[##_list_rep_title_##]`: 글의 제목
	- `[##_list_rep_rp_cnt_##]`: 댓글 수
	- `[##_list_rep_author_##]`: 작성자 이름

## 예
```
// 스킨
<s_list>
	<div class="searchList">
		<h3>'[##_list_conform_##]'에 해당되는 글 [##_list_count_##]건</h3>
		<ol>
			<s_list_rep>
				<li>
					<span class="date">[##_list_rep_regdate_##]</span>
					<a href="[##_list_rep_link_##]">[##_list_rep_title_##]</a>
					<span class="cnt">[##_list_rep_rp_cnt_##]</span>
				</li>
			</s_list_rep>
		</ol>
	</div>
</s_list>
```

```
// 변환 예
<div class="searchList">
	<h3>'업데이트 소식'에 해당되는 글 2건</h3>
	<ol>
		<li>
			<span class="date">2016.01.25</span>
			<a href="/2289">1월 초대장이 배포되었습니다.</a>
			<span class="cnt">8</span>
		</li>
		<li>
			<span class="date">2015.12.22</span>
			<a href="/2283">12월 초대장이 배포되었습니다.</a>
			<span class="cnt">19</span>
		</li>
	</ol>
</div>
```
