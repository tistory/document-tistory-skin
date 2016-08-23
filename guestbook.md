# 방명록

- url : `/guestbook`

## 방명록 영역
- `<s_guest>` : 방명록으로 접근시 이 영역 내부의 치환자가 출력됩니다.

## 입력 폼
- `<s_guest_input_form>` : 방명록을 달기 위한 입력폼을 출력합니다
	- `[##_guest_textarea_body_##]` : 글 내용 입력박스 이름
	- `[##_guest_onclick_submit_##]` : 입력 완료 온클릭 이벤트
	- `<s_guest_member>` : 로그인을 하지 않았거나 블로그 소유자가 아닌경우 보여지는 영역
		- `<s_guest_form>` : 로그인을 하지 않았을경우 보여지는 영역
			- `[##_guest_input_name_##]` : 이름입력 박스 이름
			- `[##_guest_name_##]` : 이름
			- `[##_guest_input_password_##]` : 비밀번호 입력 박스 이름
			- `[##_guest_password_##]` : 비밀번호
			- `[##_guest_input_homepage_##]` : 홈페이지 입력 박스 이름
			- `[##_guest_homepage_##]` : 홈페이지

## 방명록 리스트 구조
- `<s_guest_container>` : 등록된 '방명록' 리스트를 출력할 영역입니다
	- `<s_guest_rep>` : '방명록' 리스트의 반복열입니다
		- `<s_guest_reply_container>` : '방명록'의 댓글 리스트를 출력할 영역입니다.
			- `<s_guest_reply_rep>` : '방명록' 댓글 리스트의 반복열입니다

## 방명록 내용 (rep 내부)
- `[##_guest_rep_id_##]` : 방명록의 고유 ID
- `[##_guest_rep_class_##]` : 방명록의 글의 목록에 반복되는 스타일 + admin 아이디 앞에 아이콘
- `[##_guest_rep_name_##]` : 글쓴사람 이름
- `[##_guest_rep_date_##]` : 글쓴 날짜
- `[##_guest_rep_desc_##]` : 글 내용
- `[##_guest_rep_onclick_delete_##]` : 답글 삭제 온클릭 이벤트
- `[##_guest_rep_onclick_reply_##]` : 답글 수정 온클릭 이벤트
