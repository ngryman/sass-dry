# sass-dry [![travis][travis-image]][travis-url]

[![Greenkeeper badge](https://badges.greenkeeper.io/ngryman/sass-dry.svg)](https://greenkeeper.io/)

[travis-image]: https://img.shields.io/travis/ngryman/sass-dry.svg?style=flat
[travis-url]: https://travis-ci.org/ngryman/sass-dry

> DRY your SASS code.


`sass-dry` helps you to factorize repetitive portions of your mixins by creating and extending
dynamic placeholders under the hood.


## Install

```sh
npm install --save sass-dry
bower install --save sass-dry
```


## Usage

```scss
@include button($color: #bada55) {
  color: $color;

  @include dry(button) {
    margin: 1rem 0;
    padding: .5rem 1rem;
    border-radius: 1rem;
    border: 1px solid;
  }
}

.order-btn {
  @include button();
}

.cancel-btn {
  @include button(red);
}
```

```css
.order-btn, .cancel-btn {
  margin: 1rem 0;
  padding: .5rem 1rem;
  border-radius: 1rem;
  border: 1px solid;
}

.order-btn {
  color: #bada55;
}

.order-btn {
  color: red;
}
```

## License

MIT © [Nicolas Gryman](https://github.com/ngryman)
