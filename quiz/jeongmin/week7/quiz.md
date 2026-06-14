### Q1. **콜백 헬(callback hell)이 발생하는 원인은**?

---

### Q2. 프로미스의 상태

다음 빈칸을 채우시오.

프로미스는 생성 직후 **(1)** 상태다. 비동기 처리가 성공하면 **(2)** 함수를 호출해 **(3)** 상태로 변경되고, 실패하면 **(4)** 함수를 호출해 **(5)** 상태로 변경된다. `fulfilled` 또는 `rejected` 상태를 통틀어 **(6)** 상태라 하며, 일단 이 상태가 되면 다른 상태로 변화할 수 없다.

---

### Q3. 다음 코드의 출력 결과를 순서대로 쓰시오.

```jsx
const p = new Promise((resolve, reject) => {
  console.log('A');
  resolve(1);
  reject(new Error('error')); // 이미 settled된 이후
  console.log('B');
});

p.then(v => console.log('C:', v))
 .catch(e => console.log('D:', e));

console.log('E');
```

---

### Q4. `then` vs `catch` 에러 처리 - 다음 두 코드의 차이점을 설명하시오.

```jsx
// 코드 A
promiseGet(url)
.then(res => console.xxx(res),
      err => console.error(err)
);

// 코드 B
promiseGet(url)
  .then(res => console.xxx(res))
  .catch(err => console.error(err));
```

---

### Q5. O/X 퀴즈

1. `then`, `catch`, `finally` 후속 처리 메서드는 프로미스를 반환하므로 연속으로 호출할 수 있다.
2. `then`의 콜백이 프로미스가 아닌 일반 값을 반환하면 프로미스 체이닝이 끊어진다.
3. 프로미스 체이닝을 사용하면 콜백 함수를 전혀 사용하지 않게 된다.
4. `fetch`는 404, 500 같은 HTTP 에러가 발생하면 프로미스를 reject한다.
5. `fetch`는 네트워크 장애나 CORS 에러로 요청이 완료되지 못한 경우에만 프로미스를 reject한다.