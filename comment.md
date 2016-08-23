# 댓글

- url : Post permalink

## 댓글 영역
- `<s_rp>` : 댓글으로 접근시 이 영역 내부의 치환자가 출력됩니다.

## 입력 폼
- `<s_rp_input_form>` : 댓글을 달기 위한 입력폼을 출력합니다
	- `[##_article_rep_id_##]` : 댓글주소. 댓글들을 구분하기위해 사용합니다. 한 화면에 있는 댓글들은 각각 고유의 값을 가지고 있습니다.
	- `[##_rp_input_comment_##]` : 댓글 입력 박스 이름
	- `[##_rp_onclick_submit_##]` : 댓글 입력 온클릭 이벤트
	- `<s_rp_member>` : 로그인을 하지 않았거나 블로그 소유자가 아닌경우 보여지는 영역
		- `[##_rp_input_is_secret_##]` : 비밀글 체크박스 이름
		- `<s_rp_guest>` : 로그인을 하지 않았을경우 보여지는 영역
			- `[##_rp_input_name_##]` : 이름입력 박스 이름
			- `[##_guest_name_##]` : 이름
			- `[##_rp_input_password_##]` : 비밀번호 입력 박스 이름
			- `[##_rp_password_##]` : 비밀번호
			- `[##_rp_input_homepage_##]` : 홈페이지 입력 박스 이름
			- `[##_guest_homepage_##]` : 홈페이지

## 댓글 리스트 구조
- `<s_rp_container>` : 등록된 '댓글' 리스트를 출력할 영역입니다
	- `<s_rp_rep>` : '댓글' 리스트의 반복열입니다
		- `<s_rp2_container>` : '댓글'의 댓글 리스트를 출력할 영역입니다.
			- `<s_rp2_rep>` : '댓글' 댓글 리스트의 반복열입니다

## 댓글 내용 (rep 내부)
- `[##_rp_rep_id_##]` : 댓글의 고유 ID
- `[##_rp_rep_class_##]` : 댓글의 글의 목록에 반복되는 스타일 + admin 아이디 앞에 아이콘
- `[##_rp_rep_name_##]` : 글쓴사람 이름
- `[##_rp_rep_logo_##]` : 댓글작성자의 대표블로그 이미지
- `[##_rp_rep_date_##]` : 글쓴 날짜
- `[##_rp_rep_desc_##]` : 글 내용
- `[##_rp_rep_link_##]` : 댓글 주소
- `[##_rp_rep_onclick_delete_##]` : 답글 삭제 온클릭 이벤트
- `[##_rp_rep_onclick_reply_##]` : 답글 수정 온클릭 이벤트
