## Q1. DOM 개념 설명

DOM이 무엇인지 설명하고, HTML 문서와 DOM의 관계를 서술하시오.

## Q2. DOM 트리 구조 그리기

다음 HTML을 기반으로 생성되는 DOM 트리 구조를 간단히 그리시오.

```html
<!DOCTYPE html>
<html>
  <body>
    <h1 id="title">Hello</h1>
    <p>DOM</p>
  </body>
</html>
```

## Q3. 노드 타입 구분하기

다음 HTML에서 각 항목이 어떤 노드에 해당하는지 쓰시오.

```html
<a href="https://example.com">Example</a>
```

| 항목 | 노드 타입 |
| --- | --- |
| `document` | ? |
| `a` | ? |
| `href` | ? |
| `Example` | ? |

## Q4. DOM 요소 취득 메서드 비교

다음 설명에 알맞은 DOM 요소 취득 메서드를 쓰시오.

1. `id` 값으로 요소 하나를 취득한다. -> `(        )`
2. CSS 선택자로 일치하는 첫 번째 요소 하나를 취득한다. -> `(        )`
3. CSS 선택자로 일치하는 모든 요소를 취득한다. -> `(        )`
4. `class` 이름으로 여러 요소를 취득한다. -> `(        )`

## Q5. DOM 조작 결과 예측하기

다음 코드 실행 후 DOM 구조는 어떻게 변하는가?

```html
<ul id="fruits">
  <li>Apple</li>
  <li>Banana</li>
</ul>
```

```js
const fruits = document.querySelector('#fruits');
const li = document.createElement('li');
li.textContent = 'Orange';
fruits.appendChild(li);
```

## Q6. innerHTML과 textContent 차이

사용자 입력값을 화면에 출력할 때 `innerHTML`보다 `textContent`를 사용하는 것이 더 안전한 이유를 설명하시오.
