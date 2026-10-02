# Lilith — Design decisions

Running log, newest first. Each entry: date, the decision, who proposed
it, and who chose it. The owner, Tankun Sriket, decides everything;
nothing here is final until the owner says so. Open questions live at the
bottom. One topic per file under [`design/`](design/).

## Decided

### 2026-10-02 — Every statement starts with a capital letter (owner)

Asked whether the variable line's punctuation was correct, lth design
claude found it was (hyphen in `writer-decided`, no comma before a shared
"and", full stop outside the closing quote, as British usage has it, so
the value stays `1000` and not `1000.`), but that an English sentence
starts with a capital. Offered: capitals required (recommended), all
lowercase, or either. The owner: "opt 1". `variables.md`.

### 2026-10-02 — How a variable is declared: correct English, the type after the name (owner)

The writer picks, per variable, who decides its type: the writer, an
analysis before running, or the JIT while running. Offered short
keywords to lock, the owner: "Lol, esolang syntax", and wrote
`writer-decides variable "<name>"`, `runtime-decides`, `compiler-decides`.
Asked where the type sits (lth design claude recommended after the name,
with `as`), the owner wrote the whole line:
`writer-decides variable "x" is the type integer with 64 bits equal to
value "1000".` Then: "gotta decide the grammar first, is the grammar
correct?" lth design claude found three mistakes ("is the type" says x
is a type; "64 bits equal to" runs together; "value" lacks "the") and
one optional change (`writer-decided`, as "user-defined"), and
recommended all four. The owner took all four: "it is". So the type goes
after the name, is written in words, and the line reads as correct
English. `variables.md`.

## Open

- **Number or text in `"1000"`**, when no type is written
  (`compiler-decided`, `runtime-decided`). lth design claude offered: the
  word in front decides (`the value "1000"` a number, another word for
  text; recommended), numbers without quotes, or anything that looks like
  a number is one. Not yet answered.
