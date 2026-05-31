# 38장 · 39장(~39.5) 퀴즈

## [38장] Q1. 빈칸 채우기

브라우저의 렌더링 과정에서 HTML을 파싱하면 **( A )** 이 생성되고,
CSS를 파싱하면 **( B )** 이 생성된다.

이 둘을 결합하여 **( C )** 를 생성하며,
**( C )** 를 기반으로 레이아웃을 계산하고 **( D )** 처리를 통해 화면에 픽셀을 그린다.

---

## [38장] Q2. O/X — 틀렸으면 올바르게 고치세요

### (1)

`async` 어트리뷰트를 사용하면 HTML 파싱과 JS 파일 로드가 비동기로 동시에 진행되며, JS 실행은 HTML 파싱이 완료된 이후에 진행된다.

( O / X )

---

### (2)

`defer` 어트리뷰트를 여러 `script` 태그에 지정하면 로드가 완료된 것부터 먼저 실행되므로 순서가 보장되지 않는다.

( O / X )

---

### (3)

렌더 트리에는 `display: none` 이 적용된 요소의 노드는 포함되지 않는다.

( O / X )

---

## [38장] Q3. 단답형

`script` 태그를 `head` 안이 아닌 `body` 요소의 가장 아래에 위치시키는 이유를 두 가지 서술하세요.

1.
2.

---

## [39장] Q4. 실행 결과를 예측하세요

```html
<ul id="fruits">
  <li class="red">Apple</li>
  <li class="red">Banana</li>
  <li class="red">Orange</li>
</ul>

<script>
  const $elems = document.getElementsByClassName("red");
  console.log($elems.length); // (1)

  for (let i = 0; i < $elems.length; i++) {
    $elems[i].className = "blue";
  }

  console.log($elems.length); // (2)
</script>
```

### 문제

- (1), (2)의 출력값을 각각 쓰세요.
- `getElementsByClassName`이 반환하는 객체의 특징을 이용하여 (2)의 결과가 나오는 이유를 설명하세요.

---

## [39장] Q5. 빈칸 채우기

노드 탐색 프로퍼티 중 **( A )** 는 자식 노드를 모두 반환하며 텍스트 노드도 포함되지만,
**( B )** 는 자식 노드 중 요소 노드만 반환한다.

마찬가지로 **( C )** 는 첫 번째 자식 노드를 반환할 때 텍스트 노드를 포함할 수 있지만,
**( D )** 는 첫 번째 자식 요소 노드만 반환한다.

이처럼 `Node.prototype` 이 제공하는 탐색 프로퍼티는 텍스트 노드를 포함하고,
`Element.prototype` 이 제공하는 탐색 프로퍼티는 **( E )** 노드만 반환한다.

---

## [39장] Q6. 다음 중 올바른 것을 고르세요

```javascript
// <div id="foo">Hello <span>world!</span></div>

const $foo = document.getElementById("foo");
```

### 보기

1. `$foo.nodeValue` → `"Hello world!"`
2. `$foo.textContent` → `"Hello world!"`
3. `$foo.firstChild.nodeValue` → `"Hello "`
4. `$foo.firstChild.textContent` → `null`

---

## Q7. 순서 배열

다음은 브라우저가 HTML 문서를 받아서 화면에 그리기까지의 과정이다.

- (A) 렌더 트리를 기반으로 레이아웃(위치·크기)을 계산한다.
- (B) CSS 파싱 후 CSSOM을 생성한다.
- (C) HTML을 바이트 → 문자 → 토큰 → 노드 순으로 파싱하여 DOM을 생성한다.
- (D) 계산된 레이아웃을 바탕으로 픽셀을 화면에 페인팅한다.
- (E) DOM과 CSSOM을 결합하여 렌더 트리를 생성한다.

---

## Q8. 코드 결함 찾기

아래 코드에는 문제가 있다.

어떤 문제인지 설명하고, 수정 방법을 한 가지 이상 제시하세요.

```html
<!DOCTYPE html>
<html>
  <head>
    <script>
      const $apple = document.getElementById("apple");
      $apple.style.color = "red";
    </script>
  </head>
  <body>
    <ul>
      <li id="apple">Apple</li>
      <li id="banana">Banana</li>
    </ul>
  </body>
</html>
```
