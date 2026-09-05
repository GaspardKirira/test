Now we have tokens.

For example:

```text
LET NAME(x) = NUMBER(20)
```

But tokens are still just separate pieces.

We need to understand how these pieces belong together.

That is the job of the parser.

A parser takes tokens and builds a structure that represents what the code means.

So:

```text
LET NAME(x) = NUMBER(20)
```

can become:

```js
{
    type: "Let",
    name: "x",
    value: 20
}
```

Our next problem is:

How do we recognize this structure from the tokens?
