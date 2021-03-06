# React Student Details

![tests](https://github.com/castynet/ifunza/actions/workflows/run-tests.yml/badge.svg)
![deploy](https://github.com/castynet/ifunza/actions/workflows/firebase-hosting-merge.yml/badge.svg)
![example workflow](https://github.com/castynet/ifunza/actions/workflows/codeql-analysis.yml/badge.svg)

---
[See the Site](https://max-ifunza.web.app/)

## External Packages

1. Ant Design - UI library.
2. Zustand - state management.
3. Firebase - File management & CI/CD.
4. React Router - Routing solution.
5. Sass - extend ant design with some custom css

## Foreign Files

1. `firebaseConfig.js` initialize firebase, the file is required by the `upload component`.
2. `store.js` zustand state management, holds the global app state.
3. `testsSetup.js` defined match media a bug fix for running tests with Jest.

## Directories

1. Elements - contains the apps elements, used by various components and instances of these components.
2. Components - contains the 3 steps and an indicator of what step the user is at.

## Tests

Each component & the `app.js` contains tests to verify that all the content is present and is getting rendered to the DOM

## Question One

```javascript
// Encoding functions
// Result: 3a4b2c1d2a
const encode = (input) => {
  // Complete function here to return 3a4b2c1d2a
};

encode(aaabbbbccdaa);
```

### :white_check_mark: Answer 01

```Javascript
const encode = (input) => {
  let encodedStr = '';
  const charArrs = input.match(/([a-zA-Z])\1*/g) || [];
  for (const charArr of charArrs) encodedStr = encodedStr + charArr.length + charArr.charAt(0);
  return encodedStr;
};

encode('aaabbbbccdaa');
```

## Question Two

```javascript
const sum = () => {
  // complete function as instructed
};
// sum(1)(2)(3)(4)()
// Logs 10
```

### :white_check_mark: Answer 02

```javascript
const sum = (a) => {
  return (b) => (c) => (d) => (e) => console.log(a + b + c + d);
};

sum(1)(2)(3)(4)();
```
