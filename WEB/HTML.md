## Tag

### <b></b>

### <p></p>

### <h1><h2><h3><h4><h5><h6>

### <!DOCTYPE html>

### <html></html>

### <head></head>

### <body></body>

### !

### option + shift + f

### <ul></ul>, <li></li>, <ol></ol>

```html
<h2>Breeds Of Chickens</h2>
<ol>
  <li>Silkie</li>
  <ul>
    <li>asdf</li>
    <li>asdf</li>
    <li>asdf</li>
  </ul>
  <li>Silkie</li>
  <li>Silkie</li>
  <li>Silkie</li>
</ol>
```

### a

### <img>

```html
<img
  src="https://upload.wikimedia.org/wikipedia/commons/5/5f/Kolm%C3%A5rden_Wolf.jpg"
  alt="안녕"
  width="100"
  height="100"
/>
```

### <alt>

### HTML5

### block element vs inline element

### div

- 그룹해서 같은 속성에 있는것들을 묵어주는 방식

### span

- 특정부분에 속성을 주기 위해서 만들어준것

### hr, br, sup, sub

### HTML 엔티티

- 1 < 6을하면 부등호 때문에 문제를 일으킬 수 있다.(이미 예약되어있기 떄문에)
- entitycode.com

## Semetic 요소

### main

### nav

### section

### article

### aside

### header

### footer

### time

### 스크린 리더

### table, tr, td, th

```html
<table>
  <tr>
    <th>Animal</th>
    <th>Average mass[kg (lb)]</th>
    <th>Maximum mass[kg (lb)]</th>
    <th>Flighted</th>
  </tr>
  <tr>
    <td>Ostrich</td>
    <td>104(230)</td>
    <td>156.8 (346)</td>
    <td>No</td>
  </tr>
  <tr>
    <td>Somali Ostrich</td>
    <td>90 (200)</td>
    <td>130 (287)</td>
    <td>No</td>
  </tr>
  <tr>
    <td>Wild Turkey</td>
    <td>13.5 (29.8)</td>
    <td>39 (86)</td>
    <td>Yes</td>
  </tr>
</table>
```

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e8efac55-fb5c-4ae0-b0f8-fe13ed147442/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e8efac55-fb5c-4ae0-b0f8-fe13ed147442/Untitled.png)

### thead, tfoot, tbody

```html
<table>
  <thead>
    <tr>
      <th>Animal</th>
      <th>Average mass[kg (lb)]</th>
      <th>Maximum mass[kg (lb)]</th>
      <th>Flighted</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Ostrich</td>
      <td>104(230)</td>
      <td>156.8 (346)</td>
      <td>No</td>
    </tr>
    <tr>
      <td>Somali Ostrich</td>
      <td>90 (200)</td>
      <td>130 (287)</td>
      <td>No</td>
    </tr>
    <tr>
      <td>Wild Turkey</td>
      <td>13.5 (29.8)</td>
      <td>39 (86)</td>
      <td>Yes</td>
    </tr>
  </tbody>
</table>
```

- thead는 kind를 나타내는 부분, tbody는 본문을 나타내는 부분, tfoot는 결과를 나타내는 부분에 명시적으로 써주면 좋다.

### colspan, rowspan

```html
<table>
  <thead>
    <tr>
      <th rowspan="2">Animal</th>
      <th colspan="2">Average Mass</th>
      <th rowspan="2">Flighted</th>
    </tr>
    <tr>
      <th>KG</th>
      <th>LB</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Ostrich</td>
      <td>104</td>
      <td>230</td>
      <td>No</td>
    </tr>
    <tr>
      <td>Somali Ostrich</td>
      <td>90</td>
      <td>200</td>
      <td>No</td>
    </tr>
    <tr>
      <td>Wild Turkey</td>
      <td>13.5</td>
      <td>29.8</td>
      <td>Yes</td>
    </tr>
  </tbody>
</table>
```

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/09a2f510-e291-4553-ac6d-5bd612b7b3b6/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/09a2f510-e291-4553-ac6d-5bd612b7b3b6/Untitled.png)

- rowspan : 가로로 몇 줄이 필요한지
- colspan : 세로로 몇 줄이 필요한지

### form

- action 함수는 양식을 제출할 때 보낼 위치를 지정

### input

```html
<form action="/tacos">
  <input type="text" placeholder="username" />
  <input type="password" placeholder="password" />
  <input type="color" />
  <input type="number" placeholder="enter a number" />
</form>
```

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/39e65341-f41b-423c-9d63-995da22127a9/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/39e65341-f41b-423c-9d63-995da22127a9/Untitled.png)

### label

```html
<form action="/tacos">
  <p>
    <label for="username">Enter a Username:</label>
    <input type="text" placeholder="username" id="username" />
  </p>
  <p>
    <label for="password">Enter a Password:</label>
    <input type="password" placeholder="password" id="password" />
  </p>
  <p>
    <label for="color">Enter a Color</label>
    <input type="color" id="color" />
  </p>
  <p>
    <label for="number">Enter a Number</label>
    <input type="number" placeholder="enter a number" id="number" />
  </p>
  <p>
    <!--for과 id가 필요없이 사용하는 방법-->
    <label
      >Enter a Number
      <input type="number" placeholder="enter a number" />
    </label>
  </p>
</form>
```

- label의 for과 input의 id를 연결시켜줘야 된다.

### button

```html
<form action="/tacos">

        <p>
            <label for="username">Enter a Username:</label>
            <input type="text" placeholder="username" id="username">
        </p>
        <p>
            <label for="password">Enter a Password:</label>
            <input type="password" placeholder="password" id="password">
        </p>
        <p>
            <label for="color">Enter a Color</label>
            <input type="color" id="color">
        </p>
        <p>
            <label for="number">Enter a Number</label>
            <input type="number" placeholder="enter a number" id="number">
        </p>
				<button type="">Submit</button>
        <button type="button">Submit</button>
        <input type="submit" value="Click me">
    </form>
</body>
```

- type가 submit로 되어있을 경우(기본 값)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/488fac1a-a11f-489d-973e-e4a862047a74/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/488fac1a-a11f-489d-973e-e4a862047a74/Untitled.png)

- type가 button으로 되어있을 경우

  → 그냥 눌러지기만 한다.

### name

### Youtube에 html 코드로 검색하기

```html
<form action="https://www.youtube.com/results">
  <input type="text" name="search_query" />
  <button>Search Youtube</button>
</form>
```

- 유튜브에 쿼리문에 맞춰서 name을 입력받는 text에다가 입력을 해주고 submit를 해주면 된다.

### checkbox

```html
<form action="/birds">
  <input type="checkbox" name="agree_tos" id="agree" checked />
  <label for="agree">I Agree Everything</label>
  <button>Submit</button>
</form>
```

- checked라는 옵션을 주면 시작할 때 체크가 된 상태로 시작한다.
- 체크 된 채로 submit 버튼을 누를 경우

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/50669a0f-0a2d-4b5c-a0fb-e3ddf784304b/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/50669a0f-0a2d-4b5c-a0fb-e3ddf784304b/Untitled.png)

- 체크 안 된 채로 submit 버튼을 누를 경우

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/cefccd9e-a6b1-480c-a566-753cb40381c2/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/cefccd9e-a6b1-480c-a566-753cb40381c2/Untitled.png)

### radio

```html
<label for="xs">XS:</label>
<input type="radio" name="size" id="xs" value="xs" />
<label for="s">S:</label>
<input type="radio" name="size" id="s" value="s" />
<label for="m">M:</label>
<input type="radio" name="size" id="m" value="m" />
```

- xs를 선택한 경우

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/db538a0f-f132-4aa3-819a-b31d5bd2ab37/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/db538a0f-f132-4aa3-819a-b31d5bd2ab37/Untitled.png)

### select

```html
<label for="meal">Please Selece an Entree</label>
<select name="meal" id="meal">
  <option value="fish">Fish</option>
  <option value="veg" selected>Vegetarian</option>
  <option value="steak">steak</option>
</select>
```

- veg를 올려놓고 submit를 한 경우

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e38d50aa-e1c8-42ee-a705-84b57d5f18d1/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e38d50aa-e1c8-42ee-a705-84b57d5f18d1/Untitled.png)

### range

```html
<label for="cheese">Amount of Cheese</label>
<input
  type="range"
  id="cheese"
  min="1"
  max="10"
  value="75"
  name="cheese_level"
/>
```

- value는 초기값te
