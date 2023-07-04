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
- `[##_guest_rep_logo_##]` : 작성자 프로필
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

## 기본 방명록 치환자
- `[##_comment_group_##]` : 기본 방명록 치환자로, **방명록 개수**, **방명록 리스트**, **방명록 작성폼**을 출력합니다.
- 기본 방명록 치환자는 서버에서 하나의 `div` 태그로 렌더링 된 후, 방명록 데이터를 받아 프론트에서 최종적으로 다음과 같이 렌더링 됩니다. (기능이 변경됨에 따라 html도 변경될 수 있습니다.)

````html
<!-- 서버에서 렌더링된 직후 -->

<div data-tistory-react-app="Comment"></div>


<!-- 전체 치환 구조 -->

<div data-tistory-react-app="Comment">
   <div class="tt-comment-cont">
      [방명록 개수 영역]
      [방명록 리스트 영역]
      [방명록 작성폼 영역]
   </div>
</div>


<!-- [방명록 개수 영역] -->

<div class="tt-box-total">
  <span class="tt_txt_g">댓글</span>
  <span class="tt_num_g">{count}</span>
</div>


<!-- [방명록 리스트 영역] -->

<div class="tt-area-reply">
  <ul class="tt-list-reply">
    <!-- 핀고정 방명록 영역 시작 -->
    <li class="tt-item-reply">
      <p class="tt_cmt_info">
        <span class="tt_img_area_reply tt_ico_fixed"></span>
        <span class="tt_txt_g">{name}님이 고정했습니다.</span>
      </p>
      <div class="tt-wrap-cmt">
        <div class="tt-box-thumb">
          <a href="{homepage}">
            <span class="tt-thumbnail" style="background-image: url("{profileImageUrl}");"></span>
          </a>
        </div>
        <div class="tt-box-content">
          <div class="tt-box-meta">
            <a href="{homepage}" class="tt-link-user">{name}</a>
            <div class="tt_cmt_profile">
              <button type="button" class="tt_btn_profile">
                <span class="tt_img_area_reply tt_ico_profile">프로필열기</span>
              </button>
            </div>
            <span class="tt_img_area_reply tt_ico_fixed" style="margin-left: 4px;"></span>
          </div>
          <div class="tt-wrap-desc">
            <p class="tt_desc">{content}</p>
          </div>
          <div class="tt-wrap-info">
            <span class="tt_date">{datetime}</span>
            <span class="tt-wrap-link-comment">
                     <a href="#" class="tt-link-comment">
                        <span class="tt_txt_g">답글</span>
                        <span class="tt_num_g">{count}</span>
                     </a>
                  </span>
          </div>
          <div class="tt-box-modify">
            <button type="button" class="tt_img_area_reply tt-button-modify">더보기</button>
            <ul class="tt-list-modify">
              <li><a href="#">고정해제</a></li>
              <li><a href="#">수정</a></li>
              <li><a href="#">삭제</a></li>
              <li><a href="#">링크복사</a></li>
            </ul>
          </div>
          <div class="tt_box_pwd" style="display: none;">
            <form class="tt_form_pwd">
              <fieldset>
                <legend class="screen_out">비밀번호 입력</legend>
                <input class="tt_inp_g" type="password" title="비밀번호" placeholder="비밀번호를 입력하세요." maxlength="12" value="">
                <button type="submit" class="tt_btn_submit" disabled="">
                  <span class="tt_img_area_reply tt_ico_check">입력하기</span>
                </button>
              </fieldset>
            </form>
          </div>
        </div>
      </div>
    </li>
    <!-- 핀고정 방명록 영역 끝 -->
    <!-- 방명록이 20개보다 많을 때 이전 댓글 버튼 영역 시작 -->
    <li>
      <button type="button" class="tt_btn_prev_more">이전 댓글 더보기</button>
    </li>
    <!-- 방명록이 20개보다 많을 때 이전 댓글 버튼 영역 끝 -->
    <!-- 일반 방명록 영역 시작 -->
    <li class="tt-item-reply rp_general">
      ...
    </li>
    <!-- 일반 방명록 영역 끝 -->
  </ul>
</div>


<!-- [방명록 작성폼 영역] -->

<!-- 로그인 시 -->
<form style="margin: 0px;">
  <div class="tt-area-write">
    <div class="tt-box-thumb">
      <span class="tt-thumbnail" style="background-image: url("{profileImageUrl}");"></span>
    </div>
    <div class="tt_wrap_write">
      <div class="tt-box-textarea">
        <div class="tt-inner-g">
          <span class="tt_txt_user">{name}</span>
          <label for="comment" class="screen_out">댓글</label>
          <div contenteditable="true" placeholder="내용을 입력하세요." class="tt-cmt"></div>
        </div>
      </div>
      <div class="tt-box-write">
        <label class="tt-xe-label">
          <input type="checkbox" name="secret" id="secret">
          <span class="tt_img_area_reply tt-xe-input-helper"></span>
          <span class="tt-xe-label-text">비밀글</span>
        </label>
        <button type="submit" class="tt-btn_register">등록</button>
      </div>
    </div>
  </div>
</form>
<!-- 비로그인 시 -->
<form style="margin: 0px;">
  <div class="tt-area-write">
    <div class="tt-box-thumb">
      <span class="tt-thumbnail" style="background-image: url("{profileImageUrl}");"></span>
    </div>
    <div class="tt_wrap_write">
      <div class="tt-box-account">
        <input type="text" title="이름" placeholder="이름" maxlength="32" value="">
        <input type="password" title="비밀번호" maxlength="12" placeholder="비밀번호" value="">
      </div>
      <div class="tt-box-textarea">
        <div class="tt-inner-g">
          <div contenteditable="true" placeholder="내용을 입력하세요." class="tt-cmt"></div>
        </div>
      </div>
      <div class="tt-box-write">
        <label class="tt-xe-label">
          <input type="checkbox" id="secret">
          <span class="tt_img_area_reply tt-xe-input-helper"></span>
          <span class="tt-xe-label-text">비밀글</span>
        </label>
        <button type="submit" class="tt-btn_register" disabled="">등록</button>
      </div>
    </div>
  </div>
</form>
````

- 기본 방명록 치환자만 작성하는 것으로 방명록 화면을 구성할 수 있습니다.
- 별도의 css를 작성하지 않아도 기본 스타일이 적용되며, css를 추가하여 원하는 디자인을 사용할 수도 있습니다.
- 로그인 상태나 권한에 따라 렌더링 되는 내용이 달라집니다.
- 기능이 추가됨에 따라 html을 수정하지 않아도 됩니다.
