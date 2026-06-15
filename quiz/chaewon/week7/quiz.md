# Promise & async/await Quiz

## Q1. 다음 중 async 함수에 대한 설명으로 옳은 것은?

1. 항상 일반 값을 반환한다.
2. 반드시 await를 포함해야 한다.
3. 항상 Promise를 반환한다.
4. catch()를 사용할 수 없다.

---

## Q2. 다음 중 `await`에 대한 설명으로 옳은 것은?

1. 프로그램 전체 실행을 멈춘다.
2. Promise를 즉시 fulfilled 상태로 만든다.
3. 현재 async 함수의 실행을 잠시 중단하고 Promise가 처리되기를 기다린다.
4. async 함수 밖에서만 사용할 수 있다.

---

## Q3. 다음 코드의 실행 결과를 작성하시오.


```jsx
async function foo() {
  console.log('A');

  await Promise.resolve();

  console.log('B');
}

foo();

console.log('C');
```

---

## Q4. 제너레이터(Generator)와 일반 함수의 차이를 설명하시오.

