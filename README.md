Generates all possible values based on a charset object and a defined value length

```javascript
const permutater = require('permutater');

permutater({
    characters : 'abcdefghijklmnopqrstuvwxyz0123456789'.split(''),
    length : 3
})
// ['aaa', 'aab', 'aac' ... '997', '998', '999'].length = 46656

permutater({
    charactersAt : {
        0 : ['0', '1', '2']
    },
    characters : 'abcdefghijklmnopqrstuvwxyz'.split(''),
    length : 2
})
// ['0a', '0b', '0c' ... '2x', '2y', '2z'].length = 78

permutater({
    charactersAt : {
        0 : ['a', 'b'],
        1 : ['-']
    },
    characters : 'abcdefghijklmnopqrstuvwxyz'.split(''),
    length : 3
})
// ['a-a', 'a-b', 'a-c' ... 'b-x', 'b-y', 'b-z'].length = 78
```
