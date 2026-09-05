Now we have a structure:

```js
{
    type: "Let",
    name: "x",
    value: 20
}
```

But this structure still does nothing by itself.

We need something that executes it.

That is the job of the interpreter.

An interpreter takes the structure of the program and performs the actions it describes.

For example:

```text
Let x = 20
```

means:

```text
store x → 20
```

And:

```text
Print x + 2
```

means:

```text
20 + 2
→ 22
```

So our next problem is:

How do we execute the structure produced by the parser?
