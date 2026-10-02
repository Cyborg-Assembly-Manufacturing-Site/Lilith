# Variables

Decided by the owner, 2026-10-02 ([`DECISIONS.md`](../DECISIONS.md)).

## Who decides the type

The writer picks, per variable, who decides its type:

```
Writer-decided variable "x" is of the type integer with 64 bits and is equal to the value "1000".
Compiler-decided variable "x" is equal to the value "1000".
Runtime-decided variable "x" is equal to the value "1000".
```

- **Writer-decided**: the writer writes the type. Nothing for the JIT to
  guess.
- **Compiler-decided**: an analysis before running decides it, where it
  can see the answer.
- **Runtime-decided**: the JIT decides while running: it watches which
  types come, compiles for them behind cheap checks, and backs out when a
  guess turns out wrong.

## The rules of the line

- **A statement is a correct English sentence**: it starts with a
  capital letter and ends with a full stop.
- **The name comes straight after `variable`**, in double quotes. The
  word before `""` says what the quoted thing is.
- **The type comes after the name**, introduced by `is of the type`, and
  is written in words: `integer with 64 bits`.
- **The value comes last**, introduced by `is equal to the value`, in
  double quotes.
- **The full stop goes outside the closing quote**, so the value is
  `1000`, never `1000.`.

## Open

- Whether `"1000"` is a number or text when no type is written.
- Which types exist besides `integer with 64 bits`.
