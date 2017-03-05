# scaffolding

Useful Sass functions and utilities.

## Why?

- You only need a small portion of style code.
- You think Sass is cool, and you try using its many features to help you manage styles.
- You want to contribute to the community by providing small snippets of Sass code for others to use.

## Installation

(I was thinking what if Sass gets package management of its own somehow.)

In NPM:

    $ npm install --save @theoryofnekomata/scaffolding

In Bower

    $ bower install --save sass-scaffolding

## Usage

(You may need to adjust paths to where the Scaffolding code is installed.)

Using classes:

```scss
@import "~/classes/presentation";
@import "~/classes/a11y";

// ...

.clearfixed-element {
  @extend ._clearfix;
}

.screen-reader {
  @extend ._sr-only;
}
```

Using functions:

```scss
@import "~/functions/maps";

$map = (a: (b: (c: 'Hello world'))); // complex map

// ...

.hello-element {
  &::after {
    content: deep-get($map, 'a.b.c');
    display: block;
  }
}
```

## Notes

The classes use [rstacruz's rscss paradigm](https://github.com/rstacruz/rscss) in order for all of them to become manageable
and compact.

## License

MIT. See [LICENSE file](https://github.com/Temoto-kun/scaffolding/blob/master/LICENSE) for details.
