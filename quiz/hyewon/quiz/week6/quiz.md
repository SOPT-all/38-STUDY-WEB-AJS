## Q1. [O/X] 틀린 경우, 올바르게 수정하세요

(1) 이벤트 핸들러 프로퍼티 방식(`$button.onclick = ...`)은 하나의 이벤트에 여러 개의 핸들러를 바인딩할 수 있다. (O/X)

(2) `removeEventListener`로 핸들러를 제거하려면, `addEventListener`로 등록할 때 사용한 것과 동일한 함수 참조를 전달해야 한다. (O/X)

(3) `addEventListener`의 핸들러를 화살표 함수로 등록하면, 핸들러 내부의 `this`는 이벤트를 바인딩한 DOM 요소를 가리킨다. (O/X)

(4) `e.stopPropagation()`을 호출하면 이벤트의 기본 동작(예: `a` 태그 클릭 시 페이지 이동)이 실행되지 않는다. (O/X)

---

## Q2. 코드 실행 결과 설명

다음 코드에서, `<li>About <span>(new)</span></li>`의 **`(new)` 부분(span)을 클릭**했을 때 콘솔에 출력되는 내용과 이유를 작성하세요.

```html
Home About (new)
```

```javascript
const $menu = document.getElementById("menu");

$menu.addEventListener("click", (e) => {
  if (e.target.tagName !== "LI") return;
  console.log("currentTarget:", e.currentTarget.id);
  console.log("target:", e.target.textContent);
});
```

---

## Q3. 빈칸 채우기

자바스크립트 엔진은 단 하나의 ( A )만 가지고 있어서, 한 번에 하나의 작업만 처리할 수 있다. 이를 ( B ) 자바스크립트 엔진이라고 부른다.

`setTimeout`, `addEventListener`, `fetch`와 같은 함수는 자바스크립트 엔진이 아닌 ( C )가 제공하는 기능이며, 이를 ( D )라고 부른다. `setTimeout`이 호출되면 콜백 함수를 즉시 실행하지 않고 ( C )에 위임하며, 지정된 시간이 지나면 콜백 함수는 ( E )에 들어가 대기한다.

( F )는 ( A )이 비어 있는지 계속 감시하다가, 비어 있으면 ( E )에서 대기 중인 작업을 꺼내 ( A )으로 옮겨 실행한다.

---

## Q4. 타이머 함수 실행 결과 쓰기

다음 코드의 실행 결과를 출력되는 순서대로 쓰고, 그 이유를 콜 스택 · 태스크 큐 · 이벤트 루프 관점에서 설명하세요.

```javascript
console.log("A");

setTimeout(() => {
  console.log("B");
  setTimeout(() => {
    console.log("C");
  }, 0);
}, 0);

setTimeout(() => {
  console.log("D");
}, 0);

console.log("E");
```
