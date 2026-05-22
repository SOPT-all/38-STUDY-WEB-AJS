# this & 클로저 개념 문제

## [22장] Q1. 빈칸 채우기

```text
this 바인딩은 함수 ( A ) 시점에 결정되며, 렉시컬 스코프는 함수 ( B ) 시점에 결정된다.

일반 함수로 호출된 함수 내부의 this에는 ( C )가 바인딩된다.

메서드 내부의 this는 메서드를 ( D )한 객체에 바인딩된다.

생성자 함수 내부의 this는 생성자 함수가 미래에 생성할 ( E )를 가리킨다.

화살표 함수는 자체 this를 갖지 않고, ( F )의 this를 그대로 사용한다.
```

---

## [22장] Q2. [O/X] 틀린 경우 올바르게 수정하세요

**(1)** 메서드 내부의 this는 항상 그 메서드를 소유한 객체를 가리킨다.

**(2)** 화살표 함수는 자체적인 this 바인딩을 갖지 않으므로, call/bind/apply로 this를 변경할 수 없다.

---

## [22장] Q3. 실행 결과를 예측하세요

```js
const obj = {
  value: 100,
  foo() {
    console.log(this.value); // (1)

    function bar() {
      console.log(this.value); // (2)
    }
    bar();
  },
};

obj.foo();
```

(1), (2)의 출력값을 각각 쓰고, (2)에서 `this`가 그렇게 결정되는 이유를 설명하세요.

---

## [22장] Q4. 실행 결과를 예측하고 이유를 설명하세요

```js
const name = "global";

const person = {
  name: "Lee",
  getName: () => {
    return this.name;
  },
};

console.log(person.getName());
```

화살표 함수를 일반 함수로 바꾸면 결과가 어떻게 달라지는지도 함께 서술하세요.

---

## [24장] Q5. [O/X] 틀린 경우 올바르게 수정하세요

**(1)** 클로저는 자바스크립트 고유의 개념으로, 함수형 프로그래밍 언어에는 존재하지 않는다.

**(2)** 외부 함수가 종료되면 해당 함수의 렉시컬 환경은 항상 즉시 메모리에서 소멸한다.

**(3)** 클로저는 상위 스코프의 식별자를 참조하고, 외부 함수보다 오래 유지될 때 의미 있는 클로저라 부른다.

---

## [24장] Q6. 실행 결과를 예측하세요

```js
function makeCounter() {
  let count = 0;
  return function () {
    return ++count;
  };
}

const counter1 = makeCounter();
const counter2 = makeCounter();

console.log(counter1()); // (1)
console.log(counter1()); // (2)
console.log(counter2()); // (3)
console.log(counter1()); // (4)
```

`counter1`과 `counter2`가 `count`를 공유하는지 여부와 그 이유를 설명하세요.

---

## [24장] Q7. 실행 결과를 예측하세요

```js
var funcs = [];

for (var i = 0; i < 3; i++) {
  funcs[i] = function () {
    return i;
  };
}

console.log(funcs[0]()); // (1)
console.log(funcs[1]()); // (2)
console.log(funcs[2]()); // (3)
```

**(1)** 결과가 예상과 다르다면 왜 그런지 설명하세요.

**(2)** `var`를 `let`으로 바꾸면 결과가 어떻게 달라지는지, 그 이유를 렉시컬 환경 관점에서 서술하세요.

---

## [24장] Q8. 다음 중 클로저에 해당하는 것을 고르고, 이유를 설명하세요

```js
// (A)
function foo() {
  const x = 1;
  function bar() {
    const z = 3;
    console.log(z); // x를 참조하지 않음
  }
  return bar;
}

// (B)
function foo() {
  const x = 1;
  function bar() {
    console.log(x);
  }
  bar(); // 외부로 반환하지 않음
}

// (C)
function foo() {
  const x = 1;
  function bar() {
    console.log(x);
  }
  return bar;
}
```
