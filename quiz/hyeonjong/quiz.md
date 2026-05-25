## Q1. 빈칸 채우기

객체는 프로퍼티의 집합이며, 프로퍼티 값이 함수인 경우 특별히 ( **A** )라고 부른다.  
ES6에서 변수명과 키가 같을 때 `{ name: name }`을 `{ name }`으로 줄이는 것을 ( **B** )이라 하고,  
`{ [key]: value }` 형태로 키를 동적으로 만드는 것을 ( **C** )이라 한다.

---

## Q2. O/X — 틀렸으면 올바르게 고치세요

**(1)** `prototype` 프로퍼티는 모든 객체가 소유한다. `( O / X )`

**(2)** 객체 리터럴 `{}`로 만든 객체의 프로토타입은 `Object.prototype`이다. `( O / X )`

**(3)** JS의 `class`는 프로토타입 기반을 폐지하고 새로운 객체지향 모델을 제공한다. `( O / X )`

---

## Q3. 실행 결과는?

```js
const key = 'age';
const user = { name: 'AJS', [key]: 25 };

console.log(user.age);
console.log(user.address);
```

---

## Q4. 실행 결과는?

```js
function Circle(radius) {
  this.radius = radius;
}
Circle.prototype.getArea = function () {
  return Math.PI * this.radius ** 2;
};

const c1 = new Circle(1);
const c2 = new Circle(2);

console.log(c1.getArea === c2.getArea);
```

---

## Q5. 실행 결과는?

```js
function Person(name) {
  this.name = name;
}
Person.prototype.sayHi = function () {
  return `Hi, ${this.name}`;
};

const me = new Person('AJS');
me.sayHi = function () {
  return `Hey, ${this.name}`;
};

console.log(me.sayHi());
delete me.sayHi;
console.log(me.sayHi());
```

---

## Q6. 빈칸 채우기

`prototype`은 ( **A** )가 가지고, `__proto__`는 ( **B** )가 가진다.  
`new`로 인스턴스를 만들면 인스턴스의 `__proto__`는 생성자 함수의 ( **C** )를 가리킨다.

---

## Q7. 빈칸 채우기

프로토타입 체인의 종점은 ( **A** )이며, 이 객체의 `[[Prototype]]` 값은 ( **B** )이다.  
체인 끝까지 프로퍼티를 찾지 못하면 ( **C** )를 반환한다.

---
