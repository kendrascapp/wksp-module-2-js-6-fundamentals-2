# 2.6.1 - Debugging

---

A programmer's job is to...

---

Writing code is only one of the many things that a programmer does.

We spend lots of time doing other things as well.

- Reading documentation
- Reading code
- **Debugging code**

---

<img src='./assets/bugs.jpg' />

---

## Bugs! Where do they come from?

- Typos
- Forgot to pass an argument
- Pass the wrong type of data as an argument
- Make wrong assumptions
- etc.

---

### Exceptions

Usually when there is a bug, the computer is unable to proceed. _This is a good thing._

When it throws an exception, you have a _starting_ point from which to start debugging.

---

⚠️ Exception location is often only a **starting point**!

The actual programmer mistake can very well be elsewhere.

_This is similar to how a human error in a factory will manifest itself only in the final product._

---

Most of the time, the computer will give you the exception needed to start fixing your problem.

---

### Example

```js
const x = 5;
const y = [1, 2, 3]

y.map(x);
```

<img src='./assets/exception1.png' />

---

#### Exception, where are you?

There are cases when

- there is no error message.
- the error message is wrong.

Possible causes are

- Infinite loop
- Error is caught somewhere else
- Bug is in the build process (covered later in the course)

---

#### Finding Exceptions

The error message is missing perhpas 5% of the time (rough).

This makes it hard to find the bug.

This is where using `console.log()` can really help.

---

Learning to `console.log` effectively is an essential part of becoming a developer.

It allows you to be independent.

_It's one of the most important parts of this course._

---

## Testing

---

- What is it?
<!-- manual testing making sure things work how you want them to in browser etc.
automated testing  validate that the function is behaving as you expect it to -->
- Why do we do it?
<!-- future-proofing your own code -->
- When do we do it?
<!-- tests validate what your code is supposed to be doing
helps isolate functions and pinpoint issues  -->

_Let's talk about test-driven development a little._
start with bugs / tests, and then develop your project
focused on producing the best code possible 
---

### What is a test?
<!-- example -->
function sum(num1, num2) {
    return num1 + num2;
}

<!-- a test: you want the test function to actually run the original function -->
function sumTest(x, y, z) {
    return sum(x, y) === z;
}

<!-- test case:  -->
sumTest(5, 5, 10);
---