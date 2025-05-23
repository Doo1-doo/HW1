## 1-1

변수 a 선언

## 1-2

변수 a를 선언합니다. 값은 아직 할당되지 않았으며 undefined 상태

변수 a에 문자열 'abc'를 할당

변수 a를 다시 var로 선언하며, 동일한 'abc' 값을 다시 할당

## 1-3

a: 문자열 'abc'에 'def'를 붙여 'abcdef'가 됨

b와 c: 처음엔 둘 다 5, 이후 b만 7로 변경

## 1-4

obj1은 객체

a는 숫자 1, b는 문자열 'bbb'를 값으로 가짐

## 1-5

obj1은 객체로 선언

a는 숫자 1을 값으로 가짐

b는 문자열 'bbb'를 값으로 가짐

obj1.a = 2는 키 a의 값을 2로 변경하는 대입문

변경 이후 obj1은 { a: 2, b: 'bbb' }의 구조를 가짐

## 1-6

obj는 객체로 선언

x는 숫자 3을 값으로 가짐

arr은 [3, 4, 5]를 값으로 가지는 배열

## 1-7

a는 숫자 10으로 선언

b는 변수 a의 값을 복사하여 10을 값으로 가짐

obj1은 c, d 속성을 가지는 객체로 선언

obj2는 obj1과 같은 객체를 참조하는 변수로 선언

obj1과 obj2는 동일한 객체를 참조하기 때문에 한쪽을 수정하면 다른 쪽에도 반영

## 1-8

a, b는 값 복사

obj1, obj2는 같은 객체 참조

b 변경은 a에 영향 없음

obj2.c 변경은 obj1.c에도 영향 

## 1-9

a, b는 값 복사

obj1, obj2는 처음엔 같은 객체 참조

b 값 변경은 a에 영향 없음

obj2에 새 객체를 할당해 obj1과의 연결이 끊어짐

이후 obj1, obj2는 서로 다른 객체 참조

## 1-10

user는 객체를 선언

changeName 함수는 같은 객체를 참조하는 newUser에서 name을 변경

user2는 user와 동일한 객체를 참조

user.name과 user2.name은 모두 'Jung'으로 변경됨

user === user2는 true이므로 if 조건은 실행되지 않음

## 1-11

user는 객체를 선언

changeName은 새 객체를 생성해 반환

user2는 user와 다른 객체

user.name은 'Jaenam', user2.name은 'Jung'

user !== user2는 true이므로 메시지가 출력됨

## 1-12

copyObject는 객체를 복사하는 함수

새로운 빈 객체 result를 생성

target의 모든 속성을 result에 복사

복사된 새 객체를 반환

얕은 복사를 수행

## 1-13

copyObject는 객체를 얕게 복사

user2는 user와 다른 새 객체

user2.name만 변경되며 user.name은 그대로 유지

user !== user2는 true이므로 메시지가 출력됨

두 객체는 값은 비슷하지만 참조는 다름

## 1-14

copyObject는 객체를 얕게 복사

user2는 user와 별도 객체지만 내부 urls는 같은 객체 참조

name은 독립적이므로 변경 시 서로 영향을 주지 않음

urls 내부 속성은 공유되므로 하나를 바꾸면 모두 바뀜

결과적으로 user.urls === user2.urls는 true

## 1-15

copyObject는 객체를 얕게 복사

user2는 user와 다른 객체이며, urls도 별도로 복사

user2.urls = copyObject(user.urls)로 내부 객체도 분리

이제 user.urls와 user2.urls는 서로 다른 객체 참조

내부 속성 변경 시 서로 영향을 주지 않음

## 1-16

copyObjectDeep는 객체를 재귀적으로 깊은 복사

입력이 객체이거나 배열이면 속성마다 다시 copyObjectDeep 호출

원시값이면 그대로 복사

중첩 객체도 완전히 분리된 새 객체 생성

참조 공유 없이 독립된 구조 생성

## 1-17

copyObjectDeep는 중첩 구조를 재귀로 깊은 복사

obj2는 obj와 완전히 분리된 새 객체

obj2 내부 수정은 obj에 영향 없음

배열 d도 복사되어 서로 다른 객체로 존재

두 객체는 구조는 같지만 값과 참조는 독립됨

# 1-18

copyObjectViaJSON는 JSON 방식으로 깊은 복사 수행

함수는 JSON으로 직렬화되지 않으므로 복사 대상에서 제거

obj2는 obj와 구조는 같지만 함수가 빠진 새 객체

obj2 수정은 obj에 영향 없음

배열과 중첩 객체도 독립적으로 복사

## 1-19

a는 선언만 되어 있어 undefined 값 가짐

obj.a는 존재하므로 1 출력

obj.b는 없는 프로퍼티로 undefined 반환

b는 선언되지 않아 ReferenceError 발생

func()는 반환값이 없어 undefined 반환으로 간주

## 1-20

arr1.length = 3은 요소 없이 길이만 설정

new Array(3)도 빈 슬롯 3개 생성

arr3는 실제로 undefined 값을 가진 요소 3개를 명시적으로 포함

arr1, arr2는 빈 슬롯, arr3는 값이 있는 슬롯

console.log 결과는 같아 보여도 내부적으로는 다름

## 1-21

arr1은 undefined 값을 가진 두 요소, arr2는 1개의 빈 슬롯과 1을 가진 요소로 구성

forEach는 빈 슬롯을 건너뛰므로 arr2는 인덱스 1만 순회

map은 arr1은 모든 요소 순회, arr2는 빈 슬롯 유지

filter는 arr1에서 falsy인 undefined만 걸러짐, arr2는 빈 슬롯 무시

reduce는 arr1은 undefined부터 시작해 011을 더함, arr2는 '1' + 1 + 1로 11 생성

## 1-22

typeof null은 오래된 JS 사양상 'object'로 출력

null == undefined는 느슨한 비교로 true

null === undefined는 타입까지 비교해 false

null === null은 동일한 값과 타입으로 true

==는 타입 강제 변환, ===는 타입까지 엄격 비교

## 2-1

(1) a는 전역에서 1로 선언

outer 함수 안에서 inner가 호출됨

inner 내부에서 var a가 호이스팅되어 지역 변수 a가 선언만 먼저 됨

따라서 console.log(a)는 undefined 출력

inner 실행 후 outer의 console.log(a)는 전역 a에 접근해 1 출력

outer 호출 이후 마지막 console.log(a)도 전역 a로 1 출력

## 2-2

매개변수 x는 함수 호출 시 1로 초기화됨

var x 선언은 호이스팅되지만, 이미 존재하는 매개변수 x와 중복되므로 무시됨

(1)에서 x는 1

(2)도 여전히 1 (변수 선언만 다시 된 것)

(3)에서 x = 2로 재할당되어 2 출력됨

## 2-3

var x = 1에서 x는 선언 및 초기화되어 1을 가짐

var x;는 이미 선언된 변수이므로 무시

var x = 2에서 x는 2로 재할당됨

## 2-4

var x는 중복 선언되어도 한 번만 처리됨

x = 1로 초기화되면 이후 두 console.log(x)는 1 출력

x = 2로 재할당 후 마지막 console.log(x)는 2 출력

## 2-5

호이스팅에 의해 함수 선언 function b()가 먼저 끌어올려짐

그다음 var b 선언이 호이스팅되지만 이미 존재하므로 무시, 단 초기화는 아래에서 실행됨

실행 순서에 따라  아직 b = 'bbb'이 실행되기 전 → b는 함수 → 출력: function b() {}

'bbb'로 재할당 → 출력: 'bbb' , 여전히 'bbb' → 출력: 'bbb' 

## 2-6

함수 선언 function b() {}는 전체가 호이스팅됨

var b는 선언만 호이스팅, 무시됨 (이미 b가 있음)

함수 실행 시 b는 처음에 함수

이후 'bbb'로 재할당되면 문자열로 바뀜

## 2-7

var b = function b() {}는 함수 표현식이므로 할당 시점까지는 b는 undefined

b는 변수로 선언되고 함수가 할당됨

이후 'bbb'로 값이 바뀜

## 2-8

a는 함수 선언문으로, 함수명 a는 스코프 전체에서 사용 가능 → a() 실행 가능

b는 익명 함수 표현식을 var에 할당 → 변수명 b로 실행 가능

c는 기명 함수 표현식으로 함수명 d는 함수 내부에서만 사용 가능

c()는 실행 가능하지만 d()는 정의되지 않아 에러 발생

## 2-9

sum은 함수 선언문이므로 호이스팅되어 먼저 호출 가능 → sum(1, 2) 정상 실행

multiply는 함수 표현식이므로 var multiply는 호이스팅되지만 값은 undefined

multiply(3, 4)는 호출 시점에 아직 함수가 할당되지 않아 TypeError 발생

## 2-10

sum은 기명 함수 표현식으로, sum 변수에 함수가 할당됨 → sum(1, 2)는 정상 실행

multiply는 undefined 상태에서 호출되므로 TypeError 발생

multiply에 함수가 할당되는 시점은 호출 이후임

## 2-11

function sum이 두 번 선언되었고, 함수 선언은 호이스팅되며 마지막 선언이 우선

따라서 두 번째 sum 함수만 실제로 사용됨

console.log(sum(3, 4)) → '3 + 4 = 7' 출력

a = sum(1, 2) → '1 + 2 = 3'이 할당됨

c = sum(1, 2) → 역시 '1 + 2 = 3'

console.log(c) → '1 + 2 = 3' 출력

# 2-12

ar sum이 호이스팅 → sum은 초기값 undefined

console.log(sum(3, 4)) 실행 시 sum은 아직 함수가 아님 → 에러 발생

이후 sum에 함수가 할당되어 sum(1, 2) 실행 가능

sum이 다시 재정의되어 문자열 출력 함수로 바뀜

## 2-13

inner 함수 내부의 var a = 3은 지역 변수 선언이며, 호이스팅으로 인해 console.log(a) 실행 

시점엔 a는 undefined

outer 내부엔 a를 새로 선언하지 않았기 때문에 전역 a = 1 사용

전역 스코프에서도 a = 1 그대로 유지

## 2-14

inner 함수는 자신을 console.dir(inner)로 출력

console.dir은 함수 객체와 함께 [[Scopes]] 내부 정보를 보여줌

[[Scopes]]에는 inner 함수가 정의된 위치의 렉시컬 환경이 포함됨

즉, inner는 outer 함수의 스코프를 클로저로 기억

[[Scopes]]에는 전역 객체와 함께 outer의 지역 변수 b가 포함되어 있음

## 2-15

b = 2는 outer 함수의 지역 변수

inner 함수는 b를 참조할 수 있는 클로저

console.log(b)는 2 출력

console.dir(inner)은 함수 inner의 구조와 함께 **[[Scopes]]**에 클로저 정보 포함

이 안에 { b: 2 }가 있음 → inner가 outer의 스코프를 기억한다는 의미

## 2-16

outer 함수 실행 시 b는 2로 선언됨

inner 함수는 b를 참조하여 console.log(b)에서 2 출력

debugger;는 개발자 도구의 중단점 역할을 하여 실행을 일시 정지함

이 지점에서 디버거를 열면 **inner의 클로저 스코프(outer의 환경)**를 확인할 수 있음

→ [[Scopes]]에 Closure (outer) { b: 2 } 포함

## 3-1

전역 컨텍스트(스크립트 최상단)에서 this는 브라우저 환경에서는 window 객체를 가리킴

window는 브라우저의 전역 객체로, 전역에서 선언된 변수나 함수는 모두 이 객체의 프로퍼티가 됨

따라서 this === window는 true

## 3-2

Node.js에서는 전역에서 this는 global 객체를 가리킴

global은 브라우저의 window와 같은 역할을 하는 Node.js의 전역 객체

따라서 전역 스코프에서는 this === global → true

## 3-3

var a = 1은 전역에서 선언된 변수이므로 window.a의 프로퍼티로 등록됨

전역 컨텍스트에서의 this는 **window**를 가리킴

따라서 a, window.a, this.a는 모두 같은 값인 1

## 3-4

var a = 1: 전역 변수로 선언되어 window.a에 등록됨

window.b = 2: 전역 객체에 직접 속성 추가 → 변수 b도 자동으로 선언됨

a, window.a, this.a는 모두 같은 값

b, window.b, this.b도 같은 참조

## 3-5

var로 선언된 변수는 configurable 속성이 false이므로 delete로 삭제되지 않음

window.변수 = 값으로 직접 추가한 속성은 configurable: true이므로 삭제 가능

delete 성공 후 해당 변수에 접근하면 ReferenceError 발생

## 3-6

func(1)은 전역 호출 → this는 브라우저 환경에서 window

obj.method(2)는 객체 메서드 호출 → this는 obj 자신

## 3-7

obj.method(1)과 obj 는 동일한 방식으로 메서드를 호출

둘 다 this는 obj 객체를 참조

객체의 프로퍼티 접근 방법 (., [])이 다를 뿐 동작은 동일

## 3-8

this는 해당 메서드를 호출한 객체를 참조

점 표기법(.)과 대괄호 표기법([])은 this 결정에 영향 없음

## 3-9

obj1.outer()는 메서드 호출 → this === obj1

innerFunc()는 일반 함수 호출 → this === window

obj2.innerMethod()는 메서드 호출 → this === obj2

## 3-10

obj.outer()는 메서드 호출 → this === obj

innerFunc1()은 일반 함수 호출 → this === window (브라우저 기준)

self에 this(obj)를 저장해 참조 → console.log(self)는 obj 출력

## 3-11

obj.outer()는 메서드 호출 → this === obj

(2) innerFunc는 화살표 함수 → this는 외부 스코프(outer 함수)의 this를 그대로 사용 → obj

## 3-12

setTimeout 안 this → window

forEach 콜백의 this → undefined (strict), window (non-strict)

이벤트 핸들러 안 this → 클릭한 DOM 요소 (#a 버튼)

## 3-13

Cat은 생성자 함수

new Cat(...)을 호출하면 새로운 객체가 생성되고 this는 그 객체를 가리킴

각각의 인스턴스(choco, nabi)는 독립된 속성(bark, name, age)을 가짐

## 3-14

func(1, 2, 3) → 일반 함수 호출 → this === window

func.call({ x: 1 }, 4, 5, 6) → call로 this를 { x: 1 }로 명시 지정

## 3-15

obj.method(2, 3) → 메서드 호출 → this === obj → this.a === 1

obj.method.call({ a: 4 }, 5, 6)→ call로 this를 { a: 4 }로 변경 → this.a === 4

## 3-16

apply는 call과 비슷하지만, 두 번째 인자를 배열로 전달

첫 번째 인자는 this로 사용할 객체

## 3-17

obj는 배열처럼 생긴 유사 배열 객체

push.call(obj, 'd') → 'd'가 obj[3]에 추가되고 length가 4로 증가

slice.call(obj) → 유사 배열 obj를 진짜 배열로 변환

## 3-18

arguments와 NodeList는 배열이 아님

slice.call(...)을 쓰면 배열로 바뀜

그래서 forEach 같은 배열 메서드 사용 가능함

## 3-19

문자열 str은 유사 배열 객체 (인덱스 접근 가능, length 있음)

Array.prototype 메서드를 call이나 apply로 문자열에 적용 가능 (읽기 전용)

## 3-20

obj는 숫자 인덱스와 length를 가진 유사 배열 객체

Array.from(obj)는 이를 진짜 배열로 변환

## 3-21

둘 다 Person 생성자를 실행하면서 this를 각각의 인스턴스에 바인딩

call은 인자를 나열, apply는 배열로 전달

## 3-22

max = (min = numbers[0])는 min = 10, max = 10을 동시에 설정

배열을 순회하며:

더 큰 값이 나오면 max 갱신

더 작은 값이 나오면 min 갱신

## 3-23

Math.max.apply(null, numbers) → 배열 numbers의 요소를 Math.max에 개별 인자처럼 전달

→ 최댓값 계산

Math.min.apply(null, numbers)

→ 최솟값 계산

## 3-24

...numbers는 배열을 펼쳐서 개별 인자로 만듦

Math.max(...numbers) → Math.max(10, 20, 3, 16, 45)

Math.min(...numbers)도 마찬가지

## 3-25

bind(obj) → this를 obj로 고정

bind(obj, a, b) → this + 앞 인자 a, b 고정 (partial application)

이후 호출되는 인자는 뒤에 붙음 (앞에 고정된 인자 유지)

## 3-26

func.name → "func" → 함수 이름 그대로 출력됨

bindFunc.name → "bound func" → bind로 생성된 함수는 자동으로 "bound " 접두어가 붙음

## 3-27

obj.outer() 호출 → this === obj

innerFunc()는 일반 함수지만

call(this)로 innerFunc의 this도 obj로 지정

## 3-28

setTimeout(this.logThis, 500) → logThis만 꺼내 실행 → this는 window

setTimeout(this.logThis.bind(this), 1000) → this를 obj로 고정한 함수 실행 → this === obj

## 3-29

obj.outer()는 메서드 호출 → this === obj

innerFunc는 화살표 함수 → 화살표 함수는 this를 외부에서 렉시컬하게 상속 → 즉, this === obj

## 3-30

add 메서드에서 arguments를 배열로 변환한 후 forEach를 사용해 각각의 값을 this.sum에 더하고 this.count를 증가시킴.

forEach 내부의 this는 this를 명시적으로 설정하여 report 객체를 참조하도록 함

## 3-31

callback 함수의 this를 지정하려면 thisArg를 두 번째 인자로 전달

this는 전역 객체(window 또는 global)를 참조,수정하려면 thisArg를 사용하여 this를 변경

## 4-1

0부터 4까지 300ms 간격으로 출력하는 동작

count가 5가 되면 타이머 중단

## 4-2

콜백 함수 cbFunc로 0부터 4까지 300ms 간격으로 출력하는 동작

count가 5가 되면 타이머 중단

## 4-3

각 배열 요소에 5를 더하고 출력 후 새로운 배열 생성

현재 값과 인덱스를 로그로 출력

## 4-4

map 함수의 인자가 순서가 잘못되어 예상과 다른 결과 생성

각 요소가 인덱스로 처리되어 5, 6, 7로 반환

## 4-5

Array.prototype.map 직접 구현 예제

콜백을 통해 각 요소에 함수 적용 후 새 배열 반환

## 4-6

setTimeout과 forEach에서 this는 window를 가리킴

이벤트 리스너에서는 this가 클릭된 버튼을 가리킴

## 4-7

메서드로 호출 시 this는 객체를 가리킴

forEach에서 전달 시 this가 window를 가리켜 의도와 다름

## 4-8

함수 내부에서 self로 this를 저장해 클로저 생성

setTimeout에서 클로저를 통해 객체의 name 출력

## 4-9

setTimeout으로 전달된 함수는 this가 obj1이 아님

직접 호출이 아닌 경우 전역 객체를 참조

## 4-10

obj2.func 호출로 즉시 실행되어 undefined 반환

call을 통해 this를 obj3으로 설정했지만 실행은 즉시 발생

## 4-11

bind를 통해 this를 명시적으로 설정한 후 setTimeout에 전달

this가 올바르게 obj1 또는 obj2로 설정되어 name 출력

## 4-12

중첩된 setTimeout으로 순차적 비동기 실행 구성

에스프레소부터 시작해 아메리카노, 모카, 라떼 순으로 출력

## 4-13

각 커피 추가 함수를 체이닝하여 순차 실행

변수 coffeeList에 이름을 누적 출력

## 4-14

Promise 체인을 이용해 비동기 작업을 순서대로 처리

커피 이름을 순차적으로 연결하여 출력

## 4-15

addCoffee 함수가 클로저와 Promise를 반환

각 단계에서 이름을 누적하며 비동기적으로 출력

## 4-16

제너레이터와 yield를 사용한 비동기 순차 처리 예제

next 호출로 커피 이름을 순차적으로 연결하여 출력

## 4-17

async/await 문법을 활용한 비동기 커피 이름 추가

await로 각 커피 이름을 순서대로 연결하여 출력

## 5-1

함수 내부에서 선언된 inner 함수로 지역 변수 a를 증가시켜 출력

outer를 실행하면 inner가 즉시 실행되어 2 출력

## 5-2

outer 함수가 inner 함수 실행 결과를 반환

outer2에 2가 저장되고 출력 결과도 2

## 5-3

inner 함수 자체를 반환해 클로저 형성

outer2를 두 번 실행할 때마다 a가 증가하여 2, 3 출력

## 5-4

클로저를 통해 상태를 기억하며 일정 간격마다 실행

a가 10 이상 되면 setInterval 해제

## 5-5

클로저 참조 해제를 통해 메모리 누수 방지 예시

함수 참조를 끊거나 이벤트 제거로 메모리 해제 유도

## 5-6

각 과일마다 클릭 이벤트를 통해 고유한 alert 출력

클로저로 fruit 값을 기억해 각 버튼이 해당 과일 출력

## 5-7

모든 li 요소에 같은 alertFruit 함수 연결

단, 클릭 시 어떤 과일인지 구분 불가

## 5-8

bind로 각 과일에 맞는 인자를 사전 결합

각 클릭 이벤트에서 해당 과일명 정확히 출력

## 5-9

클로저를 생성하는 함수로 각 과일에 맞는 핸들러 생성

각 li 클릭 시 해당 과일 이름을 정확히 출력

## 5-10

객체에 연료, 연비 정보를 포함한 자동차 동작 구현

run 메서드로 연료를 소모하며 이동 거리 누적

## 5-11

자동차 객체를 함수로 생성하고 일부 속성만 외부 제공

연료 정보는 외부에서 접근 불가하며 run으로만 동작

## 5-12

Object.freeze로 외부에서 속성 변경 불가 처리

불변 객체를 반환하여 보다 안전한 상태 유지 가능

## 5-13

bind로 일부 인자를 고정한 새로운 함수 생성

미리 고정된 인자에 추가 인자를 더해 합산 수행

## 5-14

직접 partial 함수 구현하여 다중 인자 고정 기능 제공

this를 유지하면서 일부 인자만 미리 결합 가능

## 5-15

빈 자리(_)를 지정해 나중에 채울 수 있는 partial 구현

bind와 비슷하지만 자리 지정이 가능해 유연성 향상

## 5-16

debounce 구현으로 이벤트 과잉 호출 방지

지정된 시간 내 추가 이벤트 발생 시 이전 타이머 제거

## 5-17

두 인자를 각각 받아 처리하는 커링 함수 예시

고정된 첫 번째 인자와 함께 max, min 연산 수행

## 5-18

다섯 단계로 인자를 받는 커링 함수 구현

순차적으로 5개의 숫자를 전달해 최대값 계산