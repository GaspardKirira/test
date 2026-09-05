So let's start with this:

```text
20 + 22
```

Right now, JavaScript sees this as text.

```js
const source = "20 + 22";
```

But we want to see three meaningful parts:

```text
20
+
22
```

So maybe our first idea is very simple:

```js
const parts = source.split(" ");
console.log(parts);
```

And we get:

```js
["20", "+", "22"];
```

Good.

But now I remove the spaces:

```text
20+22
```

What happens?

```js
const source = "20+22";
const parts = source.split(" ");

console.log(parts);
```

Now we get:

```js
["20+22"];
```

So our first solution works only when the user writes spaces.

That is a problem.

We don't want the user to write code for our lexer.

We want the lexer to understand the code.

So instead of asking:

"Where are the spaces?"

we can ask:

"What are the things I want to find?"

For now, we only need:

```text
numbers
and operators
```

So we can search for them:

```js
const pattern = /\d+|[+\-*/]/g;
const parts = source.match(pattern) ?? [];

console.log(parts);
```

Now both of these work:

```text
20 + 22
20+22
```

And both give us:

```js
["20", "+", "22"];
```

At this point, we have solved our first problem.

We can recognize the meaningful pieces of our source code.

But we still have another problem.

For JavaScript, `"20"` is still a string.

We want our language to know:

```text
20 is a NUMBER
+ is an operator
22 is a NUMBER
```

So now we need to turn these pieces into tokens.
