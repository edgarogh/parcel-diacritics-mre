Minimal Working Example of Parcel/Babel miscompiling JSX string literal (non-expression) attributes containing diacritics.

Extremely simple example:

```jsx
const café0 = (<img alt="café"/>).props.alt;
const café1 = (<img alt={"café"}/>).props.alt;

console.log("café0 = %s, café1 = %s", café0, café1); // « café0 = caf\xe9, café1 = café »
```

As we can see, the expression version on line 2 works, but not the literal string one.
