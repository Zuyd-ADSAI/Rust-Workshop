---
title: Rust Workshop
version: 1.0.0
theme: default
class: invert
footer: ![width:80px](img/ferris.png) 
header: 
paginate: true
marp: true
backgroundColor: #515151
color: #fff
style: |
    img[alt~="center"] {
      display: block;
      margin: 0 auto;
    }
---
<style>
h1 {
  text-align: center;
}
</style>

<h1> Rust Workshop - ADSAI </h1> 


![w:500 center](img/rust-logo-blk-invert.svg)

---

## Plan for today:

- $\pm$ 1 hour presentation
- coffee break
- $\pm$ 2 hours hands-on Rust workshop

<!-- > # In rust, you tell the compiler how the world works. It will hold you and everyone who contributes to your code accountable to the contract you have written. -->

---

# What is Rust?

Rust is a programming language focusing on: 
- **Speed**
- **Memory safety** 
- **Parallelism**

---

# What is Rust?

Rust is designed to be **safe** and supports styles from multiple paradigms:
- pure-functional
- imperative-procedural
- object-oriented

---

## StackOverflow developer survey 2024
https://survey.stackoverflow.co/2024/technology#2-programming-scripting-and-markup-languages

![w: 100 center](img/stackoverflow-dev-survey-2024-technology-admired-and-desired-language-desire-admire-social.png)

---

# A little more motivation

- What do we mean by safe?
- What is memory safety?

---

# Age old problem of memory safety


![w:1000 center](img/TimelineOfProgrammingLanguages.png)

---

Consider this pseudo code
```
function main() {
  String s = "hello world"


}
```

---

# Explaining Rust by example
- Errors
- Correctness
- Options
- Results

---

# No Error

JavaScript:
```javascript
let spam = ['cat', 'dog', 'mouse']
console.log(spam[6])
``` 
- No output
- No error's
- Just an `undefined`

---

# Bad Error

Python:
```python
spam = ['cat', 'dog', 'mouse']
print(spam[6])
``` 
Python ~~error~~ traceback
```
Traceback (most recent call last):
  File "segfaults.py", line 2, in <module>
    print(spam[6])
IndexError: list index out of range
```

---

# Good Error

Rust:
```rust
let spam = ["cat", "dog", "mouse"];
println!("{}", spam[6])
``` 
Rust error ~~traceback~~
```
error: this operation will panic at runtime
 --> no_segfaults.rs:2:15
  |
2 |     println!("{}", spam[6]);
  |                    ^^^^^^^ index out of bounds: 
        the length is 3 but the index is 6
```

---

# Handle errors

Find the differences
```python
int(item["ViewCount"]["N"])
```
```rust
i32::from_str_radix(
    item["ViewCount"].unwrap()
        .get("N").unwrap(),
    10
).unwrap()
```


---

# Is this funtion correct?

```rust
function add_one(n) {
    return n + 1;
}
``` 
...it depends

---

# Is this funtion correct?

```rust
function add_one(n) {
    return n + 1;
}
``` 
...it depends, on:
- Is `n` always a number?
- How large is `n`?
- Could `n` be modified while we're reading its value?
- and so on...

---

# Options Everywhere

You can't always get want you want
```rust
enum Option<T> { // T can contain any type of value
    Some(T),
    None,
}

let possibly_a_number = Some(1);
possibly_a_number.map(|n| n + 1).unwrap_or(0); // = 2

let another_number = None;
another_number.map(|n| n + 1).unwrap_or(0); // = 1
```

---

# Results Everywhere

When things go south, you need another route
```rust
enum Result<T, E> { 
    Ok(T), // T can contain any type of value
    Err(E), // E can contain any type of Error
}
```

---

Zero cost abstractions

---

Make Invalid States Unrepresentable

---

---

---

---

---

---

# The real Copilot

##### Rust compiler:
- Won't let you crash

---
