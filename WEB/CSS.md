# CSS

### link

```html
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Css Intro</title>
  <link rel="stylesheet" href="app.css" />
</head>
```

- 다른 파일에 있는 css를 불러오는 기능

### color, background-color, background

```css
button {
  color: magenta;
  background-color: cyan;
}

p {
  color: oldlace;
  background: orange;
}
```

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/55c5292a-77cc-4244-b468-5a6a629824d3/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/55c5292a-77cc-4244-b468-5a6a629824d3/Untitled.png)

## CSS에서 색상을 나타내는 방법

### RGB

→ 0부터 255사이에 값, 0이면 그 색은 없는 것

```css
background-color: rgb(89, 151, 0);
```

### 16진수

#2(red)2(green)2(blue)

## CSS TEXT

```css
text-align: ; text를 어디로 정렬할것인지
font-weight: ; Text의 굵기를 나타냄
text-decoration: ; text에 줄을 치는것 ex) orange underline
line-height: ; 줄 간격
letter-spacing: ; 글자 사이 간격
font-size: ; 글자 크기
font-family: ;
```

## Selector

### universal selector

```css
* {
  color: block;
}
```

→ 전체를 바꾸는 css

### Elemetnt Selector

```css
img {
  width: 100px;
  height: 200px;
}
```

→ 특정 단어를 선택해서 스타일을 바꾸는 css

### Selector List

```css
h1,
h2 {
  width: 100px;
  height: 200px;
}
```

→ 2개 이상의 요소를 선택해서 바꾸는 것

### ID Selector

```css
#signup {
  background-color: pink;
}
```

→ 각 요소의 id를 추출해서 css style를 바꾸는 형식

### Class Selector

```css
.complete {
  color: orange;
}
```

→ 가장 많이 사용하는 것

→ 태그가 달라도 똑같은 css를 적용할 수 있다는 장점

### Descendant Selector

```css
li a {
  color: teal;
}
```

→ li 태그 안에 있는 a 태그를 나타내는 것

→ 멀리 떨어져 있는 자손도 태그 2개로 나타낼 수 있다.

### Adjacent Selector

```css
h1 + p {
  color: red;
}
```

→ h1 바로 뒤에 오는 p태그를 다 바꿔주는 css

### Direct Child

```css
div > li {
  color: red;
}
```

### Attribute Select

```css
input[type="text"] {
  width: 300px;
  color: yellow;
}
```
