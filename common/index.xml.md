# 스킨 정보 파일

스킨에 필요한 정보를 담고 있는 xml 파일로 이 파일이 변경되면 스킨의 모든 설정이 초기화됩니다.

```xml
<?xml version="1.0" encoding="utf-8"?>
<skin>
  <information>
    <name>기본 스킨</name>
    <version>1.1</version>
    <description>
      <![CDATA[웹표준을 준수한 XHTML 기반의 Tistory 기본 스킨입니다.]]>
    </description>
    <license>
      <![CDATA[자유롭게 수정이 가능하며, 저작권 표시하에 재배포 가능합니다.]]>
    </license>
  </information>
  <author>
    <name>tistory</name>
    <homepage>http://notice.tistory.com</homepage>
    <email>tistoryblog@daum.net</email>
  </author>
  <default>
    <recentEntries>5</recentEntries>
    <recentComments>5</recentComments>
    <recentTrackbacks>5</recentTrackbacks>
    <itemsOnGuestbook>10</itemsOnGuestbook>
    <tagsInCloud>30</tagsInCloud>
    <sortInCloud>3</sortInCloud>
    <expandComment>0</expandComment>
    <expandTrackback>0</expandTrackback>
    <lengthOfRecentNotice>25</lengthOfRecentNotice>
    <lengthOfRecentEntry>27</lengthOfRecentEntry>
    <lengthOfRecentComment>30</lengthOfRecentComment>
    <lengthOfRecentTrackback>30</lengthOfRecentTrackback>
    <lengthOfLink>30</lengthOfLink>
    <showListOnCategory>1</showListOnCategory>
    <showListOnArchive>1</showListOnArchive>
    <commentMessage>
      <none>댓글이 없습니다.</none>
      <single>댓글 &lt;span class="cnt"&gt;하나&lt;/span&gt; 달렸습니다.</single>
    </commentMessage>
    <trackbackMessage>
      <none>받은 트랙백이 없고</none>
      <single>트랙백이 &lt;span class="cnt"&gt;하나&lt;/span&gt;이고</single>
    </trackbackMessage>
    <tree>
      <color>000000</color>
      <bgColor>ffffff</bgColor>
      <activeColor>000000</activeColor>
      <activeBgColor>eeeeee</activeBgColor>
      <labelLength>27</labelLength>
      <showValue>1</showValue>
    </tree>
    <contentWidth>500</contentWidth>
  </default>
</skin> 
```

## 기본 정보

스킨 목록, 상세보기에서 표시되는 정보입니다.

- name: 표시되는 이름
- version: 스킨 버전
- description: 스킨 상세 설명
- license: 저작권


## 제작자

스킨 정보에서 표시할 제작자 정보입니다.

- name: 표시되는 이름
- homepage: 제작자 웹사이트 주소
- email: 연락할 이메일 주소


## 설정 기본값

스킨의 설정 기본값입니다. 이를 통해 스킨 적용하면 제작자가 추천하는 설정을 제공할 수 있습니다.

- recentEntries: 사이드바의 최근글 표시 갯수
- recentComments: 사이드바의 최근 댓글 표시 갯수
- recentTrackbacks: 사이드바의 최근 트랙백 표시 갯수
- itemsOnGuestbook: 한페이지에 표시될 방명록 갯수 ***
- tagsInCloud: 사이드바에 표시될 태그 갯수
- sortInCloud: 태그 클라우드 표현 방식 (1:인기도순, 2:이름순, 3:랜덤)
- expandComment: 댓글영역 표현 방식 (0:감추기, 1:펼치기)
- expandTrackback: 트랙백영역 표현 방식 (0:감추기, 1:펼치기)
- lengthOfRecentNotice: 최근 공지 표현될 글자수
- lengthOfRecentEntry: 최근 글 표현될 글자수
- lengthOfRecentComment: 최근 댓글에 표현될 글자수
- lengthOfRecentTrackback: 최근 트랙백에 표현될 글자수
- lengthOfLink: 링크에 표현될 글자수
- entriesOnPage: 홈 화면 글 수
- entriesOnList: 글 목록 글 수
- showListOnCategory: 커버 미사용 홈에서 글 목록 표현(0:내용만, 1:목록만, 2: 내용+목록)
- showListLock : 홈 설정과 기본 설정에서 '목록 구성 요소' 항목의 노출 여부 결정 (0: 노출, 1: 노출 안 함)
- tree: 카테고리
  - color: 카테고리 글자색
  - bgColor: 카테고리 배경색
  - activeColor: 선택시 글자색
  - activeBgColor: 선택시 배경색
  - labelLength: 표현될 카테고리 글자 수
  - showValue: 카테고리 글 수 표현(0:숨김, 1:보임)
  - contentWidth: 콘텐츠영역 가로 사이즈, 이 사이즈에 맞춰 에디터의 위지윅이 제대로 구현된다.
- cover: 홈 커버 기본값으로 자세한 내용은 ['홈 커버 > 기본값'](cover.md#기본값) 장에서 설명합니다.


## 홈 커버

홈 커버에 사용한 아이템을 정의합니다. 자세한 내용은 ['홈 커버 > 정의'](cover.md#정의-indexxml) 장에서 설명합니다.


## 스킨 옵션

스킨 옵션에서 제공할 옵션을 정의합니다. 자세한 내용은 ['스킨 옵션 > 옵션 정의'](variable.md#옵션-정의-indexxml) 장에서 설명합니다.


## 리스트 스타일

사용할 수 있는 글 목록 스타일을 정의합니다. 자세한 내용은 ['리스트 > 리스트 스타일'](../list/list.md#리스트-스타일) 장에서 설명합니다.
