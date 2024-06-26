
# `text-emphasis-skip`

## Syntax

```css
/* Initial value */
text-emphasis-skip: none;

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
- `dutch`
  - : All capitals, and all vowels skipped, and `ij` is considered a vowel.
- `lowercase`
  - : All lowercase characters skipped.
- `vowels`
  - : All vowels skipped.

## Examples

### Dutch Example

```css
em {
  font-style: normal;
  text-emphasis: "\0301";
  text-emphasis-skip: capitals vowels;
}
```
