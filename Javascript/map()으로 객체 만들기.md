```jsx
let testArr1 = ["aaa", "bbb", "ccc", "ddd", "eee"];
let testArr2 = [1, 2, 3, 4, 5];
let testObj = testArr1.map((v, i) => ({ type : v, number : testArr2[i] }));
console.log(testObj);
```
