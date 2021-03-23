# Codewars

## Kata Level 6 - Find The Parity Outlier

---

## Challenge

You are given an array (which will have a length of at least 3, but could be very large) containing integers. The array is either entirely comprised of odd integers or entirely comprised of even integers except for a single integer `N`. Write a method that takes the array as an argument and returns this "outlier" `N`.

## Solution

```
const findOutlier = (integers) => {
  const sampleArray = [integers[0], integers[1], integers[2]];

  const evenOddChecker = [integers[0], integers[1], integers[2]].filter(
    (integer) => {
      return integer % 2 === 0;
    }
  );

  if (evenOddChecker.length > 1) {
    return integers.find(integer => integer % 2 !== 0)
  } else {
    return integers.find(integer => integer % 2 === 0)
  }
};
```
