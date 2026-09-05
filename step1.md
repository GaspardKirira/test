Good morning everyone.

Today, we are going to build a very small programming language with JavaScript.

A programming language is simply a way for us to write instructions that a computer can understand.

For example:

```text
let x = 20
print x + 2
```

We understand this easily.

But the computer does not start by seeing variables, numbers, or operations.

It starts with text.

So we need a few steps to move from text to execution.

The first step is called a lexer.

A lexer takes source code and breaks it into meaningful pieces called tokens.

For example:

```text
20 + 22
```

can become:

```text
20
+
22
```

and then:

```text
NUMBER
+
NUMBER
```

So our first problem is simple:

How do we take source code and recognize these meaningful pieces?
