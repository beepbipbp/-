# false로 인식되는 것들
- 비어있는 문자열 ""
- 0
- null
- undefined
- NaN

# true로 인식되는 것들
- 객체
- 배열
- 비어있지 않은 문자열
- 0이 아닌 숫자
- Date
---
### !!을 사용하여 위의 값들을 boolean값으로 반환하게 할 수 있다.
> 예시
> ``` javascript
> // false 반환
> console.log(!!"");
> console.log(!!0);
> console.log(!!null);
> console.log(!!undefined);
> console.log(!!NaN);
>
> // true 반환
> console.log(!!{a: "aa", b: "bb", c: "cc"});
> console.log(!![1, 2, 3]);
> console.log(!!{}); // 비어있는 객체와 배열도 true로 인식된다.
> console.log(!![]);
> console.log(!!"example");
> console.log(!!123);
> console.log(!!(new Date()));
> ```
