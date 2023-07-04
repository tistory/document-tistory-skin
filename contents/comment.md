# 댓글

## 댓글 그룹
- `<s_rp>` : 댓글으로 접근시 이 영역 내부의 치환자가 출력됩니다.

```html
<s_rp>
  <div class="comment">
    <h3>댓글을 달아 주세요 </h3>
    <div class="commentList">18-6-1 리스트 </div>
    <div class="commentWrite">18-6-2 글쓰기 </div>
  </div>
</s_rp>
```

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

```html
<s_rp_input_form>
  <div class="commentWrite">
    <s_rp_member>
      <s_rp_guest>
        <p>
          <input type="text" name="[##_rp_input_name_##]" value="[##_guest_name_##]" />
          <label for="name"> : 이름 </label>
        </p>
        <p>
          <input type="password" maxlength="8" name="[##_rp_input_password_##]" value="[##_rp_admin_check_##]" />블로그 관리자일 경우 password field에 미리 비밀번호를 넣어놓기 위해 만들어 놓았던 치환자였으나, 지금은 사용되지 않음.. (현재는 블로그 관리자일 경우 password field가 나타나지
          않음.)
          <label for="password"> : 패스워드 </label>
        </p>
        <p>
          <input type="text" class="homepage" name="[##_rp_input_homepage_##]" value="[##_guest_homepage_##]" />
          <label for="homepage"> : 홈페이지 </label>
        </p>
      </s_rp_guest>
      <p class="secretWrap">
        <input type="checkbox" name="[##_rp_input_is_secret_##]" class="checkbox" />
        <label for="secret"> 비밀글 </label>
      </p>
    </s_rp_member>
    <p>
      <textarea name="[##_rp_input_comment_##]" rows="10" cols="50"></textarea>
    </p>
    <p>
      <input type="submit" value="댓글 달기" onclick="[##_rp_onclick_submit_##]" />
    </p>
  </div>
</s_rp_input_form>
```

## 댓글 리스트 구조
- `<s_rp_container>` : 등록된 '댓글' 리스트를 출력할 영역입니다
	- `<s_rp_rep>` : '댓글' 리스트의 반복열입니다
		- `<s_rp2_container>` : '댓글'의 댓글 리스트를 출력할 영역입니다.
			- `<s_rp2_rep>` : '댓글' 댓글 리스트의 반복열입니다

## 댓글 내용 (rep 내부)
- `[##_rp_rep_id_##]` : 댓글의 고유 ID
- `[##_rp_rep_class_##]` : 댓글의 글의 목록에 반복되는 스타일 + admin 아이디 앞에 아이콘
- `[##_rp_rep_name_##]` : 글쓴사람 이름
- `[##_rp_rep_logo_##]` : 댓글작성자의 프로필 이미지
- `[##_rp_rep_date_##]` : 글쓴 날짜
- `[##_rp_rep_desc_##]` : 글 내용
- `[##_rp_rep_link_##]` : 댓글 주소
- `[##_rp_rep_onclick_delete_##]` : 답글 삭제 온클릭 이벤트
- `[##_rp_rep_onclick_reply_##]` : 답글 수정 온클릭 이벤트

```html
<div class="commentList">
  <s_rp_container>
    <ol>
      <s_rp_rep>
        <li id='[##_rp_rep_id_##]'>
          <div class="[##_rp_rep_class_##]">
            <span class="image">[##_rp_rep_logo_##]</span>
            <span class="name">[##_rp_rep_name_##]</span>
            <span class="date"> [##_rp_rep_date_##]</span>
            <span class="control">
              <a href="[##_rp_rep_link_##]" class="address">&nbsp;
                <span>댓글주소</span>
              </a>
              <a href="#" onclick="[##_rp_rep_onclick_delete_##]" class="modify">&nbsp;
                <span>수정/삭제</span>
              </a>
              <a href="#" onclick="[##_rp_rep_onclick_reply_##]" class="write">&nbsp;
                <span>댓글쓰기</span>
              </a>
            </span>
            <p>[##_rp_rep_desc_##]</p>
          </div>
          <s_rp2_container>
            <ul>
              <s_rp2_rep>
                <li id='[##_rp_rep_id_##]'>
                  <div class="[##_rp_rep_class_##]">
                    <span class="image">[##_rp_rep_logo_##]</span>
                    <span class="name">[##_rp_rep_name_##]</span>
                    <span class="date"> [##_rp_rep_date_##]</span>
                    <span class="control">
                      <a href="[##_rp_rep_link_##]" class="address">&nbsp;
                        <span>댓글주소</span>
                      </a>
                      <a href="#" onclick="[##_rp_rep_onclick_delete_##]" class="modify">&nbsp;
                        <span>수정/삭제</span>
                      </a>
                    </span>
                    <p>[##_rp_rep_desc_##]</p>
                  </div>
                </li>
              </s_rp2_rep>
            </ul>
          </s_rp2_container>
        </li>
      </s_rp_rep>
    </ol>
  </s_rp_container>
</div>
```

## 기본 댓글 치환자
- `[##_comment_group_##]` : 기본 댓글 치환자로, **댓글 개수**, **댓글 리스트**, **댓글 작성폼**을 출력합니다.
- 기본 댓글 치환자는 서버에서 하나의 `div` 태그로 렌더링 된 후, 댓글 데이터를 받아 프론트에서 최종적으로 다음과 같이 렌더링 됩니다. (기능이 변경됨에 따라 html도 변경될 수 있습니다.)

````html
<!-- 서버에서 렌더링된 직후 -->

<div data-tistory-react-app="Comment"></div>


<!-- 전체 치환 구조 -->

<div data-tistory-react-app="Comment">
   <div class="tt-comment-cont">
      [댓글 개수 영역]
      [댓글 리스트 영역]
      [댓글 작성폼 영역]
   </div>
</div>


<!-- [댓글 개수 영역] -->

<div class="tt-box-total">
  <span class="tt_txt_g">댓글</span>
  <span class="tt_num_g">{count}</span>
</div>


<!-- [댓글 리스트 영역] -->

<div class="tt-area-reply">
  <ul class="tt-list-reply">
    <!-- 핀고정 댓글 영역 시작 -->
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
    <!-- 핀고정 댓글 영역 끝 -->
    <!-- 댓글이 20개보다 많을 때 이전 댓글 버튼 영역 시작 -->
    <li>
      <button type="button" class="tt_btn_prev_more">이전 댓글 더보기</button>
    </li>
    <!-- 댓글이 20개보다 많을 때 이전 댓글 버튼 영역 끝 -->
    <!-- 일반 댓글 영역 시작 -->
    <li class="tt-item-reply rp_general">
      ...
    </li>
    <!-- 일반 댓글 영역 끝 -->
  </ul>
</div>


<!-- [댓글 작성폼 영역] -->

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

- 기본 댓글 치환자만 작성하는 것으로 댓글 화면을 구성할 수 있습니다.
- 별도의 css를 작성하지 않아도 기본 스타일이 적용되며, css를 추가하여 원하는 디자인을 사용할 수도 있습니다.
- 로그인 상태나 권한에 따라 렌더링 되는 내용이 달라집니다.
- 기능이 추가됨에 따라 html을 수정하지 않아도 됩니다.
