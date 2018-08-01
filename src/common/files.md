# 파일구조

```
SKIN ─┬─ index.xml
      ├─ skin.html
      ├─ style.css
      ├─ preview.gif
      ├─ preview256.jpg
      ├─ preview560.jpg
      ├─ preview1600.jpg
      └─ images ─┬─ script.js
                 ├─ background.jpg
                 ├─ background.jpg
                 └─ background.jpg
```

## index.xml

스킨 정보 파일로 자세한 내용은 ['스킨 정보 파일'](index.xml.md) 장에서 다룹니다.


## skin.html

스킨의 메인 템플릿 파일로 치환자를 사용해 각 url에 해당하는 HTML 결과물로 치환됩니다.


## style.css

css 분리를 위한 파일이며 `skin.html`과 마찬가지로 스킨에디터에서 편집할 수 있습니다.


## preview

티스토리 각 영역에서 미리보기를 표시하기 위한 파일압니다.

- preview.gif : 미리보기 기본 파일로 아래 파일이 없는 경우에 사용
- preview256.jpg : 사용 중인 스킨 미리보기
- preview560.jpg : 스킨 목록 미리보기
- preview1600.jpg : 스킨 상세보기 미리보기
