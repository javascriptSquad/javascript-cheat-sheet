# Replacing Text In Strings

- Author: [funnyboy-roks](https://github.com/funnyboy-roks)

Strings can often have text in them that you don't want to be the same, for example, replaceing new lines with commas, or removing all occurances of a certain character.

## Information

Reference Material:

- [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/replace)

## Examples and Explanation

We can do a simple `String.replace()` for the first occurance of a string in another string using the following:

```js
let myString = 'I think JavaScript is very fun!';

myString = myString.replace('think', 'know');
//                          Original Replace

console.log(myString); // 'I know JavaScript is very fun!'
```

This is very useful if you're wanting to replace a single occurance, however, most of the time we want to do all occurances.
To do this, we need to use a Regular Expression, like so

```js
let myString = 'The dog jumped over the cat. The cat did not like the dog, so the cat ran from the dog.';

myString = myString.replace(/dog/g, 'ferret'); // In order to replace globally, we need to use the regular expression `g` flag.

console.log(myString); // 'The ferret jumped over the cat. The cat did not like the ferret, so the cat ran from the ferret'
```

We can also use a lambda function instead of the replacement string.  This can be useful if we want to replace with different values based on the text.

```js
let myString = 'The dog jumped over the cat. The cat did not like the dog, so the cat ran from the dog.';

myString = myString.replace(/(dog|cat)/g, (str) => {
    switch (str) {
        case 'dog':
            return 'ferret';
        case 'cat':
            return 'fox';
    }
});

console.log(myString); // 'The ferret jumped over the fox. The fox did not like the ferret, so the fox ran from the ferret.'
```
