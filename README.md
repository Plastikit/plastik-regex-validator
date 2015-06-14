plastik-regex-validator
============

`plastik-regex-validator` validates user input against a specified regular expression.

Demos and documentation are available on the 
[component page](https://www.plastikit.org/1.x/components/plastik-regex-validator/).

Pull requests are always welcome. If you encounter any bugs, please feel free to
[submit an issue](https://github.com/Plastikit/plastik-regex-validator/issues/new/).

## Installation

```sh
bower install Plastikit/plastik-regex-validator --save
```

## Basic usage

 > _See [component page](https://www.plastikit.org/1.x/components/plastik-regex-validator/)
 > for more details._

Regular expressions are executed against the entire input string. Therefore, it is
important to use `^` and `$` as necessary to ensure that the entire string conforms
to the desired restrictions.

### Example

```html
    <input is="iron-input" bind-value="{{value}}">

    <plastik-regex-validator regex="/^[0-9]$/" input="[[value]]" valid="{{isValid}}">
    </plastik-regex-validator>

    <label hidden$="[[isValid]]">Invalid input! Digits only.</label>
    <label hidden$="[[!isValid]]">Valid digit-only input!</label>
```