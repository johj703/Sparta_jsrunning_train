# Sparta_jsrunning_train

달리기반 실습 과제입니다.  
1일차에 배운 내용들을 토대로 풀 수 있도록 구성되어 있습니다.

&nbsp;

## 1. 빈칸 채우기 문제

아래 내용에서 빈 칸에 들어갈 항목들을 채워주시고 왜 그렇게 생각했는지
본인의 생각을 간단하게 1줄 정도 같이 적어주세요.

```javascript
1. let uninitialized;
console.log(uninitialized);
// 결과값 => undefined
// => 이유는 uninitialized 변수가 선언만 되었지 값이 할당되지 않았기 때문에 콘솔에 undefined이 뜨는 것이라고 생각 합니다.


2. const apple = "사과";
apple = "바나나";
// TypeError: Assignment to constant variable
// => const로 선언된 변수는 상수(변하지 않는 값) 값을 유지하고 값을 재할당을 할 수 없기 때문에 TypeError Error가 나타난다고 생각 합니다.


3. let lotto = [3, 8, 13, 19, 21, 32];
console.log(lotto[3]);
// 결과값 => 19
// 배열의 내부 값들은 index라는 번호를 0부터 가지게 되는데 lotto배열의 3번째 index는 lotto배열의 값을 순서대로 0번째 값은 3, 첫 번째 값은 8, 두 번째 값은 13, 세 번째 값은 19기 때문에 lotto[3]의 콘솔 값은 19로 나타난다고 생각 합니다.


4.
let mySchedule = "";
console.log(mySchedule || false);
// 결과값 => false
// false가 나타난 이유는 "||(or)" 연산자는 "||" 기준으로 왼쪽, 오른쪽의 값 중 하나의 값이 true나 false가 있다면 결과 값은 true, false가 됩니다. 그래서 문제에 있는 "mySchedule", "false" 이 두개의 인자 중 false는 boolean 타입의 false이므로 결과 값이 false로 나온 것 입니다.
console.log(!!mySchedule);
// 결과값 => false
// mySchedule의 값은 비어있는 string 값입니다. 빈 문자열의 boolean 값은 false입니다. 그리고 mySchdule 앞에 있는 "!" 연산자는 부정 연산자로 boolean의 값을 반대로 출력하게 만들어 줍니다. 그러나 "!"가 두 번 찍혀있으니 이중부정으로 원래의 boolean 값을 나타내게 되므로 false가 나타나게 됩니다.

```

&nbsp;

## 2. 객체 선언해보기

지난 시간에 배웠던 객체(object)를 다시 복습해보며, 아래의 조건을 충족하는 객체를 직접 선언해보세요.

- 자기 자신을 소개하는 객체입니다.
- 이름, 나이, MBTI 세 가지 키와 값이 포함되어 있어야 합니다.
- 콘솔 창에 이름, 나이, MBTI가 나오도록 console.log() 를 찍어보세요.

예시

```javascript
const junhyun = {
    // 조건을 충족하는 코드 작성
};

console.log(이름이 나오게 콘솔을 실행시켜 주세요.);
console.log(나이가 나오게 콘솔을 실행시켜 주세요.);
console.log(MBTI가 나오게 콘솔을 실행시켜 주세요.);
```

HyunJun's 답

```javascript
const hyunjun = {
  name: "Jo Hyun-Jun",
  age: 34,
  MBTI: "ESFJ",
};

console.log(hyunjun.name);
console.log(hyunjun.age);
console.log(hyunjun.MBTI);
```

&nbsp;

## 3. 홀짝 판별기

지난 시간에 배웠던 연산자를 활용하여, 숫자를 입력하면 홀수인지 짝수인지 판별하는 함수를 만들어 보려고 합니다. 다음과 같은 결과값이 나올 수 있도록 코드를 작성해 주세요.

예시

```javascript
function 함수명(매개변수) {
  // 코드를 작성해 주세요.
}

console.log(함수명(10)); // 결과값 "짝수";
console.log(함수명(7)); // 결과값 "홀수";
```

HyunJun's 답

```javascript
function oddEven(num) {
  if (num % 2 == 1) {
    console.log("홀수");
  } else {
    console.log("짝수");
  }
}

console.log(oddEven(10)); // 결과값 "짝수";
console.log(oddEven(7)); // 결과값 "홀수";
```

&nbsp;

## 4. 계산기 문제

연산자와 함수, 조건문을 토대로 계산기 함수를 하나 만들어 보려고 합니다.
함수에 숫자 , 연산자 , 숫자 세 개의 매개변수를 넣었을 때 해당 연산자를 기준으로 연산을 해서 값을 반환하는 함수를 만들어주세요.

예시

```javascript
function 함수명(매개변수1, 매개변수2, 매개변수3) {
  // 코드를 작성해주세요.
}

함수명(3, "+", 6); // 결과값 9
함수명(11, "-", 6); // 결과값 5
함수명(6, "*", 3); // 결과값 18
함수명(15, "/", 3); // 결과값 5
```

Hyunjun's 답

```javascript
function calculate(num1, operSymbol, num2) {
  let result = 0;
  switch (operSymbol) {
    case "+":
      result = Number(num1) + Number(num2);
      break;
    case "-":
      result = Number(num1) - Number(num2);
      break;
    case "*":
      result = Number(num1) * Number(num2);
      break;
    case "/":
      result = Number(num1) / Number(num2);
      break;
  }
  return String(result);
}

calculate(3, "+", 6); // 결과값 9
calculate(11, "-", 6); // 결과값 5
calculate(6, "*", 3); // 결과값 18
calculate(15, "/", 3); // 결과값 5
```

&nbsp;

## 5. 평균 점수 구하기 [선택 문제]

5번 문제는 필수 문제가 아닌, 4번까지 풀고 여유가 있을 때 풀어보는 선택 문제입니다.

&nbsp;

학교에서 시험을 보았는데 전산 문제로 한 문제의 답이 전부 오답처리가 된 바람에 학생들의 점수를 전부 3점씩 올려주어야 합니다.

scores에 있는 학생들의 점수를 반복문을 통해 3점씩 올리게 고쳐주시는데 4번 문제를 통해 만든 계산기 함수를 통해 더해주세요.

```javascript
const scores = [36, 62, 72, 55, 86, 95, 92, 48, 81];

function 함수명(scores) {
  // 4번 문제의 계산기 함수를 활용한 코드를 작성해주세요.
}

console.log(scores);
// 기대값: [39, 65, 75, 58, 89, 98, 95, 51, 84]
```
