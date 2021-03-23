# Codewars

## Kata Level 6 - ounting Duplicates

---

## Challenge

Write a function that will return the count of distinct case-insensitive alphabetic characters and numeric digits that occur more than once in the input string. The input string can be assumed to contain only alphabets (both uppercase and lowercase) and numeric digits.

## Solution

```
const duplicateCount = (text) => {
  const stringArray = text.split('');

  const letterCounter = stringArray.reduce((counter, letter) => {
    letter = letter.toLowerCase()
    counter[letter] = counter[letter] + 1 || 0;
    return counter;
  }, {});

  const sumTotalCount = Object.keys(letterCounter).reduce(
    (total, letterKey) => {
      if (letterCounter[letterKey] > 0) {
        total++
      }
      return total;
    },
    0
  );

  return sumTotalCount;
};
};
```
