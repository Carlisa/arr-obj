
# arr-obj

 [![PayPal](https://img.shields.io/badge/%24-paypal-f39c12.svg)][paypal-donations] [![AMA](https://img.shields.io/badge/ask%20me-anything-1abc9c.svg)](https://github.com/IonicaBizau/ama) [![Version](https://img.shields.io/npm/v/arr-obj.svg)](https://www.npmjs.com/package/arr-obj) [![Downloads](https://img.shields.io/npm/dt/arr-obj.svg)](https://www.npmjs.com/package/arr-obj) [![Get help on Codementor](https://cdn.codementor.io/badges/get_help_github.svg)](https://www.codementor.io/johnnyb?utm_source=github&utm_medium=button&utm_term=johnnyb&utm_campaign=github)

> Convert arrays into objects by using unique fields.

## :cloud: Installation

```sh
$ npm i --save arr-obj
```


## :clipboard: Example



```js
const arrObj = require("arr-obj");

let arr = [
    { name: "Alice", location: { name: "Earth" } },
    { name: "Bob", location: { name: "Mars" } }
];

console.log(arrObj(arr, "name"));
// { Alice: { name: 'Alice', location: { name: 'Earth' } },
//   Bob: { name: 'Bob', location: { name: 'Mars' } } }

console.log(arrObj(arr, "location.name", true));
// { Earth: { name: 'Alice', location: { name: 'Earth' } },
//   Mars: { name: 'Bob', location: { name: 'Mars' } } }

console.log(arrObj([1, 4, 9, 16], c => {
    return Math.sqrt(c);
}));
// { '1': 1, '2': 4, '3': 9, '4': 16 }
```

## :memo: Documentation


### `arrObj(arr, by, deep)`
Convert an array into object by using unique fields.

#### Params
- **Array** `arr`: The input array.
- **String|Function** `by`: The field name to use in the object keys or a function returning this value.
- **Boolean** `deep`: Use this for accessing nested objects in the array elements.

#### Return
- **Object** The result object.



## :yum: How to contribute
Have an idea? Found a bug? See [how to contribute][contributing].


## :scroll: License

[MIT][license] © [Ionică Bizău][website]

[paypal-donations]: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=RVXDDLKKLQRJW
[donate-now]: http://i.imgur.com/6cMbHOC.png

[license]: http://showalicense.com/?fullname=Ionic%C4%83%20Biz%C4%83u%20%3Cbizauionica%40gmail.com%3E%20(http%3A%2F%2Fionicabizau.net)&year=2016#license-mit
[website]: http://ionicabizau.net
[contributing]: /CONTRIBUTING.md
[docs]: /DOCUMENTATION.md
