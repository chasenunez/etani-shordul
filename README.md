# bookbot

Reads a plain-text book and prints word count plus a letter-frequency ranking. The name's a nod to **etaoin shrdlu** — the rough order of letter frequency in English text — and one of the small joys of running it on Frankenstein is that the output really does start `e, t, a, o, i, n, s, h, r, d`.

## Run

```bash
python3 main.py books/frankenstein.txt
```

Drop `.txt` files (Project Gutenberg is full of them) into a `books/` folder. Anything plain-text will work.

## Files

- `main.py` — entry point
- `stats.py` — counting and ordering helpers
- `books/` — sample text files

## Example output

```
============ BOOKBOT ============
Analyzing book found at books/frankenstein.txt...
----------- Word Count ----------
Found 75767 total words
--------- Character Count -------
e: 44538
t: 29493
a: 25894
o: 24494
i: 23927
n: 23643
s: 20360
r: 20079
h: 19176
d: 16318
l: 12306
m: 10206
u: 10111
c: 9011
...
æ: 28
â: 8
ê: 7
ë: 2
ô: 1
============= END ===============
```

The accented letters at the bottom are a surprisingly reliable fingerprint — Frankenstein has 28 instances of `æ` because of all the "encyclopædia"-style spellings from 1818.
