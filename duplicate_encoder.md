# Codewars

## Kata Level 6 - Duplicate Encoder

---

## Challenge

The goal of this exercise is to convert a string to a new string where each character in the new string is `"("` if that character appears only once in the original string, or `")"` if that character appears more than once in the original string. Ignore capitalization when determining if a character is a duplicate.

## Solution

```
const duplicateEncode = (word) => {
  const splitWord = word.split('');
  const parentheses = [];
  splitWord.forEach((word) => parentheses.push('('));

  for (let i = 0; i < splitWord.length; i++) {
    splitWord.forEach((word, index) => {
      word = word.toLowerCase();
      if (i !== index) {
        if (splitWord[i].toLowerCase() === word) {
          parentheses[i] = ')';
        }
      }
    });
  }

  return parentheses.join('');
}
```
