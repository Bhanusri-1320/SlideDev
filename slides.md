---
# You can also start simply with 'default'
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cover.sli.dev
# some information about your slides (markdown enabled)
title: Welcome to Slidev
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# https://sli.dev/guide/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/guide/syntax#mdc-syntax
mdc: true
---

# Destructuring

---

<v-clicks style="text-align: center;">

# Unpacking

<br>

<img src="public/image.png" alt="Unpacking" style="width: 600px; height: 400px; display: inline-block; margin: 0 auto;" />

</v-clicks>

---

# Types

<v-clicks>

## Array Destructuring

<br>

## Object Destructuring

</v-clicks>

---

<v-clicks>

<br>

# Array Destructuring

- Index
  <br>

```js
// Example Array
const numbers = [1, 2, 3, 4, 5];
```

```js
const [first, second, third, fourth, fifth] = numbers;
```

```js
const [first, second, ...rest] = numbers;
```

```js
console.log(first); // 1
```

```js
console.log(second); // 2
```

```js
console.log(rest); // [3, 4, 5]
```

</v-clicks>

---

<v-clicks>

## Default Values

<br>

```js
const numbers = [1, 2, 3, 4, 5];
```

```js
const [first = 8, second, third, fourth, fifth, sixth = 10] = numbers;
```

```js
console.log(first); //1
```

```js
console.log(sixth); //10
```

```js
const array = [1, 2, 3, null];
```

```js
const [one, two, three, four = 10] = array;
```

```js
console.log(four); // null
```

```js
// To skip any value
const [t1, , t2] = numbers;
```

```js
console.log(t1); //1
```

```js
console.log(t2); // 3
```

</v-clicks>

---

<v-clicks>

# Object Destructuring

- Keys

  <!-- <img src="public/image-2.png" alt="Unpacking" style="width: 50px; height: 50px; display: inline-block; margin: 0 auto;" /> -->

<br>

```js
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 30,
};
```

```js
console.log(person.firstName);
```

```js
console.log(person.lastName);
```

```js
console.log(person.age);
```

<br>

- Problem: DRY ❌

</v-clicks>

---

## Solution

<br>

<v-clicks>

```js
const { firstName, lastName, age } = person;
```

```js
console.log(firstName); // 'John'
```

```js
console.log(lastName); // 'Doe'
```

```js
console.log(age); // 30
```

```js
const { firstName, ...rest } = person;
```

```js
console.log(firstName); // 'John'
```

```js
console.log(rest); // {lastName: 'Doe', age: 30}
```

</v-clicks>

---

<v-clicks>

## Default Values

<br>

```js
// Example object
const user = {
  firstName: "John",
  lastName: "Doe",
};
```

```js
// Object destructuring with default values
const { firstName, lastName, age = 35 } = user;
```

```js
console.log(firstName); // 'John'
```

```js
console.log(lastName); // 'Doe'
```

```js
console.log(age); // 35 (default value assigned since 'age' is not defined in 'person')
```

</v-clicks>

---

<v-clicks style="text-align: center;">

<img src="public/image-1.png" alt="Thank you " style="width: 800px; height: 500px; display: inline-block; margin: 0 auto;" />

</v-clicks>
