class: center, middle

# Global State in Ruby

## Frank West
---
class: center, middle

## What is global state?

--

Global state is a way of sharing data across the entirety if your application.

---

## Types of global state

The most common forms of global state in ruby programs are:

* Global Variables

--

* Constants

--

* Environment Variables

--

These are not the only types of global state, but they are the most common in our day to day
programming.

---


## The Good

* Singleton Classes

--

* Environment Variables

--

* Constants

Even these can be problematic and should be used carefully. When using global state you should take
every precaution to ensure these values are immutable.

---


## Immutability in global state

We can combat some of these problems by making our global state immutable.

Some of the tools available to us are:

* String#freeze

--

* Hamster - https://github.com/hamstergem/hamster

--

* Common sense

---

## The bad

* Unreliablility and unpredictable

--

* Makes code highly couples to implementation

--

* Breaks encapsulation

--

* Random errors and test failures

--

* Makes code readability harder

--

* Concurrency issues

---

## Can we avoid global state?

--

Generally, no. Global state is something that usually can't be avoided.

--

Ruby has built in global state.

--

Most of these are defined by the `$` implementation.

* $! - The exception information message. raise sets this variable.
* $@ - The backtrace of the last exception, which is the array of the string that indicates the point where methods invoked from.
* $stdin - The current standard input.
* $VERBOSE - The verbose flag, which is set by the -v switch to the Ruby interpreter.
* And many more.

--

Most of our applications also use ENV variables to manage global state.

The key is to be responsible with our use.

---

## Ruby's class variables and global variables

--

* @@state = "I am available in every instance of my class"

--

* $global_variable = "I am available everywhere"

---

## Some examples

* Random spec failures

--

* Rails controller/view bugs

---

## Ways to avoid global state

--

* Function parameters

--

* Dependency Injection

--

* Immutable global state

--

* Immutable singletons

--

* Dynamic binding

---

class: center, middle

# Thank you

