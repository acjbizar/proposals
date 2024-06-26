
# `text-emphasis-skip`

## Syntax

```css
/* Initial value */
text-emphasis-skip: none;

/* <string> values */
text-emphasis-skip: "a";

/* Keyword values */
text-emphasis-skip: capitals;
text-emphasis-skip: consonants;
text-emphasis-skip: lowercase;
text-emphasis-skip: vowels;
```

### Values

- `none`
  - : No characters skipped.
- `capitals`
  - : All capital characters skipped.
- `consonants`
  - : All consonants skipped.
- `lowercase`
  - : All lowercase characters skipped.
- `numbers`
  - : All numeral characters skipped.
- `vowels`
  - : All vowels skipped.

## Examples

### Dutch Emphasis

```css
em:lang(nl) {
  font-style: normal;
  text-emphasis-style: "\0301";
  text-emphasis-skip: capitals vowels "ij";
}
```
