## Flow

- Exact Object Types

In Flow, it is considered safe to pass an object with extra properties where a normal object type is expected.

```js
// @flow
function method(obj: { foo: string }) {
  // ...
}

method({
  foo: "test", // Works!
  bar: 42 // Works!
});
```

Sometimes it is useful to disable this behavior and only allow a specific set of properties. For this, Flow supports “exact” object types.

```js
{| foo: string, bar: number |}
```
