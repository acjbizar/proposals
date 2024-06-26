
# Threading Text

## Introduction

Hypertext currently has no mechanism to have (text) content flow into a different container when the initial container runs out of space. This has been an indispensable feature of desktop publishing like [InDesign](https://helpx.adobe.com/indesign/using/threading-text.html) for decades, and is clearly missing from Web publishing.

## Why CSS

The proposed functionality mostly concerns the structure and semantics of a document. Therefor, the main proposal is actually for HTML. However, a CSS rule could be used to opt in or out of the default proposed visual representation.

## Rules

```CSS
.box {
    overflow: thread, hidden;
}
```
