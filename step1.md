Good morning everyone.

Today, I want to build something simple with you.

Not a framework.
Not a library.
A programming language.

But we are not going to start with compilers, parsers, or theory.

We are going to start with a problem.

Imagine I write this:

```text
let x = 20
print x + 2
```

For us, this is easy to understand.

We can read it and say:

`x` is 20.

Then:

20 + 2 = 22.

But for the computer, this is just text.

So our first question is:

How can we take this text and make the computer understand what is inside it?

Let's start with something even smaller:

```text
20 + 22
```

The first thing we need is to recognize:

```text
20
+
22
```

So we have our first problem:

How do we break source code into meaningful pieces?
