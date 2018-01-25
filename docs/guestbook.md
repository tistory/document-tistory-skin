# 방명록

## 방명록 그룹
- `<s_guest>` : 방명록 그룹치환자

```html
<s_guest>
  <div class="guestbook">
    <h3>방명록</h3>
    <div class="guestWrite">입력 폼</div>
    <div class="guestList">리스트</div>
  </div>
</s_guest> 
```

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

```html
<s_guest_input_form>
  <div class="guestWrite">
    <s_guest_member>
      <s_guest_form>
        <div>
          <input type="text" name="[##_guest_input_name_##]" value="[##_guest_name_##]" />
          <label for="name"> : 이름 </label>
        </div>
        <div>
          <input type="password" maxlength="8" name="[##_guest_input_password_##]" value="[##_guest_password_##]" />
          <label for="password"> : 패스워드 </label>
        </div>
        <div>
          <input type="text" name="[##_guest_input_homepage_##]" value="[##_guest_homepage_##]" />
          <label for="homepage"> : 홈페이지 </label>
        </div>
      </s_guest_form>
    </s_guest_member>
    <div>
      <textarea name="[##_guest_textarea_body_##]" cols="50" rows="6"></textarea>
    </div>
    <div>
      <input type="submit" value="안부 남기기" onclick="[##_guest_onclick_submit_##]"/>
    </div>
  </div>
</s_guest_input_form>
```

## 리스트
- `<s_guest_container>` : 방명록 리스트 그룹치환자
	- `<s_guest_rep>` : 방명록 정보 그룹치환자
		- `<s_guest_reply_container>` : '방명록'의 댓글 리스트를 출력할 영역입니다.
			- `<s_guest_reply_rep>` : '방명록' 댓글 리스트의 반복열입니다

### 내용 (rep 내부)
- `[##_guest_rep_id_##]` : 방명록의 고유 ID
- `[##_guest_rep_class_##]` : 방명록의 글의 목록에 반복되는 스타일 + admin 아이디 앞에 아이콘
- `[##_guest_rep_name_##]` : 글쓴사람 이름
- `[##_guest_rep_date_##]` : 글쓴 날짜
- `[##_guest_rep_desc_##]` : 글 내용
- `[##_guest_rep_onclick_delete_##]` : 답글 삭제 온클릭 이벤트
- `[##_guest_rep_onclick_reply_##]` : 답글 수정 온클릭 이벤트

```html
<s_guest_container>
  <div class="guestList">
    <ol>
      <s_guest_rep>
        <li id='[##_guest_rep_id_##]'>
          <div class="[##_guest_rep_class_##]">
            <span class="name">[##_guest_rep_name_##]</span>
            <span class="date"> [##_guest_rep_date_##]</span>
            <span class="control">
              <a href="#" onclick="[##_guest_rep_onclick_delete_##]">MODIFY/DELETE</a>
              <a href="#" onclick="[##_guest_rep_onclick_reply_##]">REPLY</a>
            </span>
            <p>[##_guest_rep_desc_##]</p>
          </div>
          <s_guest_reply_container>
            <ul>
              <s_guest_reply_rep>
              <li id='[##_guest_rep_id_##]'>
                <div class="[##_guest_rep_class_##]">
                  <span class="name">[##_guest_rep_name_##]</span>
                  <span class="date"> [##_guest_rep_date_##]</span>
                  <span class="control">
                    <a href="#" onclick="[##_guest_rep_onclick_delete_##]">MODIFY/DELETE </a>
                  </span>
                  <p>[##_guest_rep_desc_##]</p>
                </div>
              </li>
              </s_guest_reply_rep>
            </ul>
          </s_guest_reply_container>
        </li>
      </s_guest_rep>
    </ol>
  </div>
</s_guest_container>
```
