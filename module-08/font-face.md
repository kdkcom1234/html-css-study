CSS의 `@font-face` 규칙을 사용하여 글꼴을 적용하고 `font-weight`를 지정하는 방법은 다음과 같습니다:

1. 웹 글꼴 파일(`.woff`, `.woff2`, `.ttf`, `.otf` 등)을 준비하고 웹 서버에 업로드합니다.

2. CSS 스타일 시트 파일에서 `@font-face` 규칙을 추가합니다. `font-weight`를 포함한 기본 구문은 다음과 같습니다:

```css
@font-face {
  font-family: "FontName";
  src: url("font-file-path.woff2") format("woff2"), url("font-file-path.woff")
      format("woff");
  font-weight: normal;
  /* 다른 포맷 및 font-weight 조합을 지원하는 경우 추가로 지정 가능 */
  /* src: url('font-file-path-bold.woff2') format('woff2'),
          url('font-file-path-bold.woff') format('woff');
     font-weight: bold; */
}
```

- `font-weight`: 글꼴의 두께를 지정합니다. 일반적으로 `normal` 또는 `bold` 값을 사용합니다. 기본값은 `normal`입니다.

3. `@font-face` 규칙을 추가한 후, 적용하려는 요소에 `font-family`와 `font-weight` 속성을 할당합니다. 예를 들어, `<h1>` 요소에 적용하려는 경우:

```css
h1 {
  font-family: "FontName", sans-serif;
  font-weight: normal;
}
```

- `'FontName'`: 이전에 `@font-face` 규칙에서 지정한 글꼴 이름입니다.
- `font-weight`: 글꼴의 두께를 지정합니다. `normal` 또는 `bold` 값을 사용합니다.

4. CSS 파일을 연결하여 웹 페이지에 적용합니다.

예를 들어, 다음과 같이 `@font-face` 규칙을 지정하고 `h1` 요소에 글꼴을 적용하고 `bold` 두께를 사용하려는 경우:

```css
@font-face {
  font-family: "CustomFont";
  src: url("fonts/custom-font.woff2") format("woff2"), url("fonts/custom-font.woff")
      format("woff");
  font-weight: normal;
}

h1 {
  font-family: "CustomFont", sans-serif;
  font-weight: bold;
}
```

이제 `h1` 요소는 `'CustomFont'` 글꼴을 `bold` 두께로 표시합니다. `@font-face` 규칙을 사용하여 글꼴을 적용하고 `font-weight`를 지정하는 방법을 설명했습니다. 원하는 글꼴과 두께를 지정하여 CSS 파일을 수정할 수 있습니다.
