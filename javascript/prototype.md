# Prototype

다른 객체지향 언어들에서 흔히 사용하는 `class` 대신, JavaScript에서는 `prototype`을 사용합니다. 실제 `class`와 다소 차이가 있어서 모조 클래스라고 부르기도 합니다.

## constructor

객체는 다른 언어들과 비슷한 형태로 생성합니다. 생성자 이름은 주로 다른 언어의 `class`처럼 PascalCase를 사용합니다.

```js
function Person(age, gender, name) {
  this.age = age;
  this.gender = gender;
  this.name = name;
}

var originerd = new Person(28, "male", "Jitae Kim");
```

`originerd`의 `constructor`는 `Person`을 가리킵니다.

```js
console.log(originerd.constructor.name); // "Person"
```

## prototype

`prototype` 객체는 각 인스턴스들이 가지는 프로퍼티나 함수를 정의합니다. Java나 ECMAScript 2015의 `class`의 메소드나 함수처럼, 각 인스턴스들에서 호출할 수 있습니다.

물론, `prototype`을 사용하지 않고 `age`나 `gender`, `name `등 처럼 프로퍼티 형태로 넣을 수 있습니다. 그렇게 되면, 모든 인스턴스들이 해당 프로퍼티를 개별적으로 가지고 있어서 효율적이지 않습니다.

반면에, `prototype`으로 정의를 하면 해당 함수를 공유하기 때문에 보다 효율적으로 사용할 수 있습니다.

```js
Person.prototype.introduce = function() {
  console.log('Hi, my name is ' + this.name + '. And I am ' + this.age + ', ' + this.gender + '.');
}

originerd.introduce(); // "Hi, my name is Jitae Kim. And I am 28, male."
```

## class function

`prototype`이 인스턴스 함수라면, `class function`은 클래스 함수입니다. Java나 ECMAScript 2015 등에서는 `static function` 등으로 제공됩니다.

`class function`은 `this` 등을 참조할 수 없으며, 인스턴스가 아닌 생성자로 직접 호출해야 합니다.

```js
Person.isValidAge = function(age) {
  return (age >= 0 && age < 150);
}

console.log(Person.isValid(28)); // true
```
