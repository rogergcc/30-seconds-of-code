---
title: formatStringOfNames
tags: array,intermediate,string,formatting
---

Given: an array containing hashes of names

Return: a string formatted as a list of names separated by commas except for the last two names, which should be separated by an ampersand.
 
 - Use `Array.prototype.map()` for only names in new array(names). Remove last element of names using `Array.prototype.pop()` and assign to a variable. And use `Array.prototype.join()` if array has values return name joins with the last value else return last name.
```js

const formatStringOfNames = (names) => {
  let namesFormat = names.map(p => p.name)
  let lastName = namesFormat.pop()
  return namesFormat.length ? `${namesFormat.join(', ')} & ${lastName}` : lastName || ''
};
```

```js
formatStringOfNames([ {name: 'Bart'}, {name: 'Lisa'}, {name: 'Maggie'} ])
// returns 'Bart, Lisa & Maggie'

formatStringOfNames([ {name: 'Bart'}, {name: 'Lisa'} ])
// returns 'Bart & Lisa'

formatStringOfNames([ {name: 'Bart'} ])
// returns 'Bart'

list([])
// returns ''
```